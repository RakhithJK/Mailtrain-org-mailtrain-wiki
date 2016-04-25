If your SMTP provider is SparkPost then you can register your Mailtrain installation to receive webhooks that notify about bounces, spam complaints and unsubscription actions.

  1. Log in to your SparkPost account
  2. Navigate to Account ⇒ [Webhooks](https://app.sparkpost.com/account/webhooks)
  3. Click on New Webhook button to open webhook settings
  4. Set Target URL to `http://yourserver/webhooks/sparkpost`
  5. You can keep `Events: ALL` setting but most of these events are not used by Mailtrain. To only select required events, click on `Events: SELECT` and check the following events: "Bounce", "Spam Complaint", "List Unsubscribe", "Link Unsubscribe"

Once all webhooks are set up your webhooks settings should look like this (replace `http://mailtrain.org` with your own domain name):

![](https://cldup.com/rR5O8ZzUR4.png)