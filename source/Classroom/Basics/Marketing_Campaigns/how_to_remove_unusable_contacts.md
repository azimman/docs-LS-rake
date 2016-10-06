---
seo:
  title: How to Remove Unusable Contacts
  description: Learn how you can delete contacts that result in bounces or spam reports.
  keywords: marketing, campaign, unusable, unwanted, contacts
title: How to Remove Unusable Contacts
weight: 0
layout: page
navigation:
  show: true
---

It is common to have contacts that result in a group unsubscribe, block, bounce, invalid email address, or spam report. Attempting to send email to these contacts can negatively impact your reputation since these contacts do not want to (and will not) receive your marketing emails. By continuing to store these contacts, you are being charged for recipients that will automatically be dropped.

The following steps will show you how to remove all of your unusable Marketing Campaigns contacts so that you won't continue to be charged for their storage.

1. When viewing your dashboard, navigate to the left hand menu and click **Suppressions**.

2. Open a specific group, such as Bounces or Spam Reports, click the settings cog in the upper right corner, then select **Download as CSV**.

    ![]({{root_url}}/images/remove_unusable_contacts_1.png)

3. Repeat step 2 for each of the groups that you want to remove (e.g. unsubscribes, spam reports etc.) and merge each of those lists into a single CSV file.

    * *Alternatively, you can download all of your contacts from Marketing Campaigns (create a segment defined by "created at" "is after" with a date from 1999 to capture all contacts, and then export that segment).*
    * *Next, upload that CSV of all contacts to our [List Assist](https://sendgrid.com/docs/Utilities/list_assist.html) tool. This will give you a CSV of all of your Marketing Campaigns contacts that exist on any of the Suppression lists.*
    * *Use that list to follow steps 4-8 below. You can find a video tutorial explaining how to use List Assist [here](https://www.youtube.com/watch?v=FiyDgCl78dk).*

4. Return to your dashboard, navigate to the left hand menu and select **Marketing**, then **Contacts**.

5. In the upper right corner click **Add List or Segment** and select **Upload CSV**.

6. You will be presented with a dialogue box. Select the option to **Create New List** and name it something obvious, like "Remove Invalid Emails."

7. Once uploaded, click the cog to the right of that new list and select **Delete**.

8. Another dialogue box will open asking if you wish to delete "all contacts associated with this list". Make sure that box is checked, and then you're good to go!

![]({{root_url}}/images/remove_unusable_contacts_2.png)
