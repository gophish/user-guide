# FAQ

## Events Aren't Showing Up on the Dashboard

If you are seeing emails being sent successfully, but aren't seeing events show up on the dashboard, it likely means there is a configuration error somewhere. You can follow these tips to help track it down.

**Check the Email Template**

You want to make sure you're using the `{{.URL}}` template tag when creating links in your emails. Then, when you launch a campaign, Gophish will fill this in with whatever you use as the "URL" field when creating the campaign.

A good way to see if this is working correctly is to send a test email to yourself when building a campaign and looking at the link. It should be the URL you used when creating the campaign with a unique `rid` parameter. So, it should look like this: `http://your_url/?rid=XXXXX`.

{% hint style="info" %}
**Tip**: Don't try to put your Gophish URL directly into a template. It's very important to use the `{{.URL}}` template tag, since that's how Gophish knows to generate the unique URL for each recipient.
{% endhint %}

**Check the Campaign URL**

If the links in the email look good and you still don't see events showing up, then the next step is to make sure the URL you're using when building a campaign is correct.

When creating a campaign, the URL field **must point to the server running Gophish and must be reachable by the person opening the emails.** This can either be the external IP address of the server, or a domain name that has a DNS A record pointing to the server's IP address.

{% hint style="info" %}
**Tip:** Remember that the campaign URL must be reachable by the recipients clicking the links. If they can't reach the Gophish server, Gophish can't record those events.
{% endhint %}

To test this, you can manually browse to the URL you're expecting to use in your campaign. Without any `rid` parameters provided, you should see a basic `404 page not found` error. You should also see a log appear in your Gophish terminal.

{% hint style="info" %}
**Tip:** Remember that if your Gophish `phish_server` configuration is set to use HTTPS that you need to include the URL in your campaign as `https://your_url`.
{% endhint %}

Once manually browsing to your URL works, you can try to send a test email to yourself when building a campaign. If it works, you should see your landing page being returned. This means that the URL will likely work when used in a campaign, assuming it is reachable by all recipients.
