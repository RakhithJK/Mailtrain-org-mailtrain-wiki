Mailtrain is able to detect bounced messages from Postfix *mail.log*. This file is only accessible for root and postfix user, so Mailtrain can't access it directly. To overcome this Mailtrain is able to read the file contents from TCP, so what you would need to do to use it, would be to *tail* the mail log to Mailtrain using *netcat* (or any other tool that can pipe data to tcp).

### Enable Postfix bounce handling

By default the posfix log reading server is not started. You need to enable it in the config (production.yaml or default.yaml or similiar) file

```yaml
postfixBounce:
  enabled: true
  port: 5699
  host: 127.0.0.1
```

You can also use the Docker environment variables descripted in the [REAMDE](https://github.com/Mailtrain-org/mailtrain#docker-environment-variables)

### Send data to Mailtrain

Next you would need to either *tail* Postfix logs in real time or alternatively, set up a cron job that periodically sends the last N lines of mail.log to Mailtrain

```
tail -F /var/log/mail.log | nc localhost 5699 -
```

You do not need to send all lines but only those that include the bounce information, so you could grep the data with `status=bounced` to keep the data to process minimal. If you send the entire log though, then Mailtrain finds these lines itself and ignores the rest.

For your convenience here's a simple systemd service script to keep the tail working

```
Description=Postfix bounce notifier

[Service]
ExecStart=/bin/sh -c '/usr/bin/tail -F /var/log/mail.log | nc localhost 5699 -'
Type=simple
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target
```

Copy this file to `/etc/systemd/system/` as `bouncetail.service` and enable it with the following commands:

```
systemctl enable bouncetail.service
service bouncetail start
```