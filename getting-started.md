# Getting Started

## Running Gophish

Now that you have gophish installed, you’re ready to run the software. To launch gophish, simply open a command shell and navigate to the directory the gophish binary is located.

Then, execute the gophish binary. You will see some informational output showing both the admin and phishing web servers starting up, as well as the database being created. This output will tell you the port numbers you can use to connect to the web interfaces.

```text
gophish@gophish.dev:~/src/github.com/gophish/gophish$ ./gophish
 2016/01/10 23:13:42 worker.go:34: Background Worker Started Successfully - Waiting for Campaigns
 2016/01/10 23:13:42 models.go:64: Database not found... creating db at gophish.db
 2016/01/10 23:13:42 gophish.go:49: Admin server started at https://127.0.0.1:3333
 2016/01/10 23:13:42 gophish.go:51: Phishing server started at http://0.0.0.0:80
```

{% hint style="info" %}
If your phishing server is set to run on TCP port 80, then you may need to run Gophish as an administrator so that it can bind to the privileged port.
{% endhint %}

## Logging In

After Gophish starts up, you can open a browser and navigate to [https://127.0.0.1:3333](https://127.0.0.1:3333) to reach the login page.

The default credentials are:

Username: admin

Password: gophish

![Login Screen](https://i.imgur.com/Yw63OGq.png)

