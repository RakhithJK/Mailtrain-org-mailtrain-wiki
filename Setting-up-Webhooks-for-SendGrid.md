If your SMTP provider is SendGrid then you can register your Mailtrain installation to receive webhooks that notify about bounces and spam complaints.

  1. Log in to your SendGrid account
  2. Navigate to Settings ⇒ [Mail Settings](https://app.sendgrid.com/settings/mail_settings)
  3. Open webhook settings in Event Notification section and click on Edit
  4. Check "Bounced" and "Mark as Spam" checkboxes and set webhook url to `http://yourserver/webhooks/sendgrid`
  5. Once you have accepted the changes make sure that Event Notification is marked as Active

Once all webhooks are set up your webhooks settings should look like this (replace `http://mailtrain.org` with your own domain name):

![](https://cldup.com/_CIrCfYnbc.png)