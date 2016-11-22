# Creating the Sending Profile

Creating a sending profile is easy for this campaign. Navigate to the "Sending Profiles" page and click "New Profile".

For my campaign, I'll be sending emails from Boyd Jenius, the system administrator. I'll use his name and email address in the "From" field.

I have my Morning Catch VM listening for inbound email on `192.168.56.101:25` so I will use that for my "Host".

> Remember: **Always** specify the port number when configuring a sending profile! Use the host:port format when specifying the Host.

You should wind up with something that looks like this:

![sending profile](http://imgur.com/KJ4GBd9.png)

If you want, you can send a test email to another recipient on the `morningcatch.ph` domain to ensure emails are relayed correctly.

After the settings are specified, click "Save Profile".