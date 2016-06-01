> This feature applies to Mailtrain v1.12+

In addition to exact matches and date ranges you can also use relative date ranges in segments where a date field is compared against current date. This allows you to create segments like "from 7 days before today to 5 days after today" where today means current date in UTC timezone.

To start create a new rule for a segment and choose a date field like Sign-up date or some custom date field (you can only use full date fields, birthday fields are not supported).

![](https://cldup.com/l1xN-K5VGb.png)

Next check the radio button for "Use relative range match" and set the start and end values for the range. Using "0 days before/after today" means current date.

![](https://cldup.com/n4h6_-ec8P.png)

Once you have created the rule, it should appear in the segment rules list

![](https://cldup.com/2Cz7CSzaSA.png)

> In case of range start the date value means the beginning of that day in UTC. In case of range end the date value means the end of that day in UTC.