> This feature applies to Mailtrain v1.12.0

Mailtrain has some built-in automation support. This is achieved through a triggering system. List maintainer can define a set of triggers that fire on some special occasion (X days after subscriber sign-up or Y days after subscriber clicked on a link in campaign Z).

### Step 1.
To create a new automation flow you need to define a "triggered campaign" first. This is the campaign sent once a subscriber hits a trigger.

![](https://cldup.com/v3VtnB5_YQ.png)

### Step 2.

You can set up the campaign just like any other campaign, there are no special configuration needed.

![](https://cldup.com/uO_m4E4mV6.png)

### Step 3.

The only difference between "normal" and "triggered" campaigns is that you can't sent the triggered campaign yourself.

![](https://cldup.com/dy0ZWx_dYl.png)

### Step 4.

Next you need to create a Trigger. Open the Automation menu and click on the "Create Trigger" button

![](https://cldup.com/v1ksCFsCcQ.png)

### Step 5.

Next you need to select a list this trigger is related to. You can't use campaigns or triggers over multiple lists, all actions must be done using the same list.

![](https://cldup.com/G0nY-ntm4D.png)

### Step 6.

Select the trigger rule. In this case we select that the Sign-up must have happened 1 day ago for this trigger to fire

![](https://cldup.com/0GNIG3uAx4.png)

### Step 7.

Once saved, the trigger should appear in the triggers list. The trigger is now set up and waits to be fired!

![](https://cldup.com/mUwx8XA0sh.png)

### Step 8.

Whenever a user matches rigger rule, a message is sent to this user. In this case the user should receive a "Welcome" email 1 day after signup. All triggers can fire once per user, so the same user can never receive the same message more than once.

![](https://cldup.com/4nfDcVFFbN.png)