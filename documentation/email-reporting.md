# Email Reporting

As of v0.6.0, Gophish supports the ability for users to report the simulated phishing emails they receive. This is to encourage users to report suspicious to their administrators, potentially catching malicious emails earlier.

Right now, we only support this reporting feature on the **server side** of things. We don't yet have actual email extensions and add ons that can be used to facilitate this reporting. If you're interested in writing one, this page explains how the reporting mechanism works.

## The Importance of Email Reporting

When running phishing simulations, we often focus solely on how many users clicked the links and submitted their credentials to the spoofed page. However, I would argue that there's just as much if not more value in focusing on who reported the emails to their administrator.

Consider a simple scenario where we send out 100 simulated phishing emails. Let's look through two possible outcomes:

* **Outcome 1** - In this outcome, only 1 user clicks the link and submits credentials. That's great! However, no one reports the email. In this case, as an administrator our users were targeted by phishing and an attacker has a valid set of credentials, yet we don't know anything has happened.
* **Outcome 2** - In this outcome, 50 users click the link and only 1 user reports it. In this case sure, more users clicked the link, but as an administrator we now know that a phishing campaign is in progress and we can start the incident response process.

Reporting suspicious emails can help prevent the impact of a phishing campaign. It's recommended to build a culture that **rewards the users who report emails**. Even something small like an email to that employee and their manager thanking them for their vigilance can go a long ways. This gives positive feedback that will encourage users to report more emails in the future.

### Start Small and Simple

Right now, we don't have native email clients that can make this a one-click experience for reporting emails. But, this isn't needed to get email reports. Instead, you can start small by creating a security@company.com email address and encouraging users to forward suspicious emails there. It's not perfect, but it's a great start.

In this case, the reporting metrics won't show up in the Gophish dashboard, but you can always add these to your reports manually later.

## How Reporting Works in Gophish

Every email sent by Gophish contains a link pointing to the [Landing Page](landing-pages.md) configured for the campaign. This URL looks like this:

```text
http://phish_server/?rid=1234567
```

The `rid` parameter specifies which recipient this link was generated for. To report an email sent by Gophish, an HTTP request needs to be made to:

```text
http://phish_server/report?rid=1234567
```

Sending this HTTP request is usually handled by a mail client extension. As indicated earlier, we're still working on getting those developed. If you're interested in helping make this happen, please [open an issue on Github!](https://github.com/gophish/gophish/issues)

