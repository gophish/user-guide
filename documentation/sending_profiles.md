# Sending Profiles
To send emails, Gophish requires you to configure SMTP relay details called "Sending Profiles".

To setup a sending profile, click the "Sending Profiles" navigation entry in the sidebar and click the "New Profile" button.

> Note: If you're looking for a good testing SMTP server, I've had good luck with [Mailhog](https://github.com/mailhog/MailHog).

![Sending Profiles](http://imgur.com/DgEu31g.png)

It's important to make sure that your "From" address is a valid email address format.

Additionally, make sure you setup your "Host" in the full `host:port` format.

To test your SMTP configuration, you can click the "Send Test Email" button:

![send test email](http://imgur.com/GjSHL6W.png)

After entering the recipient details and clicking "Send", you should see a message indicating if the email was sent successfully.