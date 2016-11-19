# Campaigns

Gophish is centered around launching campaigns. This involves sending emails to one or more groups and monitoring for opened emails, clicked links, or submitted credentials.

## Launching a Campaign

To configure and launch a campaign, click the "Campaigns" entry in the navigation sidebar.

![New Campaign](http://imgur.com/LUxGi2w.png)

Most of the fields should be self-explanatory. Gophish has autocompletion setup for many of the fields that are selecting from existing objects (such as landing pages, templates, etc.).

The `URL` field is what populates the `{{.URL}}` template value. This should be a URL or IP address that points to the Gophish phishing server and is reachable by the recipient.

Since version 0.2, Gophish supports scheduling campaigns, making it easy to plan campaigns in advance.

After you have the campaign configuration ready to go, click the "Launch Campaign" button, click through the confirmation message, and you're good to go!

## Viewing Campaign Results
When a campaign is launched, you are automatically redirected to the campaign results screen:

[screenshot coming soon!]