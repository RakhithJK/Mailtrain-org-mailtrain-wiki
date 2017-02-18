There are two ways to send emails using Amazon SES. The more obvious one is to use SMTP like with any other provider. Unfortunately this might not be the best solution as AWS is more API oriented and using SMTP might be a bit complicated. Even though Mailtrain has supported using SES with SMTP from day one, version v1.21.0 added support for the SES API as well.

### IAM credentials

The IAM role should minimally look like this, the magic rule being `ses:SendRawEmail`:

```json
{
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "ses:SendRawEmail",
            "Resource": "*"
        }
    ]
}
```

### Set up Mailtrain

Once you have generated IAM access credentials to use SES, you can provide these to Mailtrain. To do this, open the Settings page and scroll to SMTP options, click on the AWS SES tab and fill up the settings.

![](https://cldup.com/MOMXbogl5Y.png)

Make sure that you have the radio button "Use SES for sending mail" checked, otherwise you are still going to use SMTP.

### Verify settings

After you have filled the credentials you check if you have everything set up correctly by hitting the "Check Mailer Config" button. Mailtrain then tries to authenticate using provided credentials and if everything works, gives you a success message.

### Additional settings

You can also use *Max connections* and *Throttling* options with SES. The *Max messages* option has no effect in this case.

When using *Throttling* be aware that SES gives you a sending rate measured in messages per second while Mailtrain measures messages per hour. So if your rate limit is 20 messages per second, then you should set the Throttling value as 72000 (that's 20 * 3600).

Also be aware that these settings are per sending process. So if you have 10 sending processes configured in Mailtrain configuration file, then you should probably divide the throttling number by 10 to not run into SES rate limits.