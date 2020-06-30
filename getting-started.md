# Getting Started

## Running Gophish

Now that you have gophish installed, you’re ready to run the software. To launch gophish, open a command shell and navigate to the directory the gophish binary is located.

Then, execute the gophish binary. You will see some informational output showing both the admin and phishing web servers starting up, as well as the database being created. This output will tell you the port numbers you can use to connect to the web interfaces.

If you're running a version of Gophish **after** v0.10.1, then temporary admin credentials are printed in these logs which you can use to login.

```text
gophish@gophish.dev:~/src/github.com/gophish/gophish$ ./gophish
 time="2020-06-30T08:04:33-05:00" level=warning msg="No contact address has been configured."
 time="2020-06-30T08:04:33-05:00" level=warning msg="Please consider adding a contact_address entry in your config.json"
 time="2020-06-30T08:04:33-05:00" level=info msg="Please login with the username admin and the password 1178f855283d03d3"
 time="2020-06-30T08:04:33-05:00" level=info msg="Starting phishing server at http://0.0.0.0:80"
 time="2020-06-30T08:04:33-05:00" level=info msg="Starting IMAP monitor manager"
 time="2020-06-30T08:04:33-05:00" level=info msg="Starting admin server at https://127.0.0.1:3333"
 time="2020-06-30T08:04:33-05:00" level=info msg="Background Worker Started Successfully - Waiting for Campaigns"
 time="2020-06-30T08:04:33-05:00" level=info msg="Starting new IMAP monitor for user admin"
```

{% hint style="info" %}
If your phishing server is set to run on TCP port 80, then you may need to run Gophish as an administrator so that it can bind to the privileged port.
{% endhint %}

## Logging In

After Gophish starts up, you can open a browser and navigate to [https://127.0.0.1:3333](https://127.0.0.1:3333) to reach the login page.

For versions of Gophish &gt; 0.10.1, the temporary administrator credentials are printed in the logs when you first execute the Gophish binary. For versions of Gophish &lt;= 0.10.1, the default credentials are:

Username: admin

Password: gophish

![Login Screen](https://i.imgur.com/Yw63OGq.png)

If you're using a version of Gophish &gt; 0.10.1, then you will be required to reset your password after logging in for the first time.

{% hint style="info" %}
If you're running a version of Gophish newer than v0.10.1 and you need to set a default administrator password, you can do so by setting the `GOPHISH_INITIAL_ADMIN_PASSWORD` environment variable.

You will still be required to change your password after logging in for the first time.
{% endhint %}



