# Creating the Template

To create the template we will use for our Morning Catch campaign, first navigate to the "Email Templates" page and click the "New Template" button.

![New Template Dialog](https://imgur.com/FPqcZOG.png)

We notice that Morning Catch comes with a webmail portal. Let’s craft a simple template that suggests the user needs to go reset their password. Obviously, this is a simple scenario, and by using the "Import Email" feature, you can import existing emails directly into gophish for a greater effect.

By clicking the "HTML" tab, we will see the editor we can use to create our HTML content:

![HTML Editor](https://imgur.com/rZN827r.png)

Since our content is pretty simple, we can just click the "Source" button and be taken to the more visual editor, which will be enough for our purposes:

![Visual Editor](https://imgur.com/elue6xK.png)

Our template will be simple for the sake of demonstration. I'll start by adding the message:

```
{{.FirstName}},

The password for {{.Email}} has expired. Please reset your password here.

Thanks,
Morning Catch IT Team
```

You'll notice we used the `{{.FirstName}}` and `{{.Email}}` template values. These will populate with the target's first name and email address when the emails are sent. This is Gophish's way to tailor emails to individuals to increase the chance of success.

Speaking of links, now we need to add our phishing link. Highlight over the word "here" and right click, exposing the following menu:

