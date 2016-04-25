If your SMTP provider is Mailgun then you can register your Mailtrain installation to receive webhooks that notify about bounces and spam complaints.

  1. Log in to your Mailgun account
  2. Click on the [Webhooks](https://mailgun.com/app/webhooks) tab
  3. Click on "Hard bounces" and "Spam Complaints" and set webhook url to `http://yourserver/webhooks/mailgun`

Once all webhooks are set up your webhooks settings should look like this (replace `http://mailtrain.org` with your own domain name):

![](https://cldup.com/70balbHXsH.png)