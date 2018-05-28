# Creating the Template

To create the template we will use for our Morning Catch campaign, first navigate to the "Email Templates" page and click the "New Template" button.

![New Template Dialog](https://imgur.com/FPqcZOG.png)

We notice that Morning Catch comes with a webmail portal. Let’s craft a simple template that suggests the user needs to go reset their password. Obviously, this is a simple scenario, and by using the "Import Email" feature, you can import existing emails directly into gophish for a greater effect.

We'll use the following subject line:

```text
Password Reset for {{.Email}}
```

You'll notice we used the `{{.Email}}` template value. This will populate with the target's email address when the emails are sent. This is Gophish's way to tailor emails to individuals to increase the chance of success.

By clicking the "HTML" tab, we will see the editor we can use to create our HTML content:

![HTML Editor](https://imgur.com/rZN827r.png)

Since our content is pretty simple, we can just click the "Source" button and be taken to the more visual editor, which will be enough for our purposes:

![Visual Editor](https://imgur.com/elue6xK.png)

Our template will be simple for the sake of demonstration. I'll start by adding the message:

```text
{{.FirstName}},

The password for {{.Email}} has expired. Please reset your password here.

Thanks,
Morning Catch IT Team
```

Speaking of links, now we need to add our phishing link. Highlight the word "here" and click the chain icon in the menu, exposing the "Link" dialog. In this dialog, we'll set the link to `{{.URL}}`, another template value, so that our link is automatically created and inserted into the email.

![Link Menu](http://imgur.com/sWLOxbg.png)

Finally, make sure the "Add Tracking Image" checkbox is checked, and click "Save Template".

