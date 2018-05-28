# Campaigns

Gophish is centered around launching campaigns. This involves sending emails to one or more groups and monitoring for opened emails, clicked links, or submitted credentials.

## Launching a Campaign

To configure and launch a campaign, click the "Campaigns" entry in the navigation sidebar.

![New Campaign](http://imgur.com/LUxGi2w.png)

Most of the fields should be self-explanatory. Gophish has autocompletion setup for many of the fields that are selecting from existing objects \(such as landing pages, templates, etc.\).

The `URL` field is what populates the `{{.URL}}` template value. This should be a URL or IP address that points to the Gophish phishing server and is reachable by the recipient.

Since version 0.2, Gophish supports scheduling campaigns, making it easy to plan campaigns in advance.

After you have the campaign configuration ready to go, click the "Launch Campaign" button, click through the confirmation message, and you're good to go!

## Viewing Campaign Results

When a campaign is launched, you are automatically redirected to the campaign results screen:

![Campaign Results](http://imgur.com/VT99DCQ.png)

On the results page, you will see overview information on the campaign status as well as detailed results for each target.

### Exporting Campaign Results

To export campaign results in CSV format, click the "Export CSV" format and select the type of results you want to export:

* **Results** - The current status for each target in the campaign.

  Contains the following fields:

  ```text
  id, email, first_name, last_name, position, status, ip, latitude, longitude
  ```

* **Raw Events** - Contains a stream of events as they occurred during the campaign.

### Completing a Campaign

To complete a campaign, click the "Complete" button and confirm that you want to mark the campaign as completed.

### Deleting a Campaign

To delete a campaign, click the "Delete" button and confirm that you want to delete the campaign.

> Note: This **cannot** be undone, so be careful when deleting a campaign!

### Viewing Result Details

Gophish makes it easy to view the campaign results in a timeline format.

To view the timeline for each recipient, expand the row with the recipient's name.

![](http://imgur.com/9GTMH2k.png)

