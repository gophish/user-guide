# Landing Pages

Landing pages are the actual HTML pages that are returned to the users when they click the phishing links they receive.

Landing pages support templating, capturing credentials, and redirecting users to another website after they submit their credentials.

> Note: Landing pages are stored in the database. Gophish generates a unique ID \(called the `rid` parameter\) for each recipient in a campaign, and uses this ID to dynamically load the correct landing page.
>
> To preview what a landing page will look like, you will need to either use the HTML editor seen below, or launch a test campaign. Simply browsing directly to the Gophish listener without specifying an `rid` parameter will display a generic 404 page.

To create a landing page, click on the "Landing Pages" entry in the sidebar and click the "New Page" button.

![Landing Pages](http://imgur.com/Tg4sDId.png)

The landing page modal supports the same HTML WYSIWYG editor shown in the Templates section.

## Importing a Site From URL

A powerful feature of Gophish is the ability to import a site from a URL. To import a site, click the "Import Site" button.

![](http://imgur.com/uqxm6iB.png)  
After entering the URL and clicking "Import", you should see the HTML of the URL populated into the editor.

## Capturing Credentials

Gophish makes it easy to capture credentials from the landing page. To capture credentials, simply select the checkbox that says "Capture Submitted Data".

> Note: Credentials are stored **in plaintext**. If you don't want to capture passwords, don't select the "Capture Passwords" checkbox. Gophish will still capture other text fields, such as usernames.

### Redirecting Users

Red team assessments are all about preventing suspicion. To prevent users from becoming suspicious after entering credentials, you may want to redirect them to the original URL.

Gophish makes it easy to redirect users after they submit credentials. To redirect users, enter a URL in the "Redirect To:" text field that appears after the "Capture Submitted Data" checkbox is selected.

> Note: Make sure to include the full URL \(including the scheme such as http:// or https://\). Otherwise, browsers may interpret the URL as being relative to the Gophish URL.

## Static Assets

There may be times that you want to store assets such as HTML pages, CSS/JS resources or other static files. To use these in Gophish, just move them under the `static/endpoint` directory. You can then reference them using the URL `http[s]://phishing_server/static/filename`. For more background, see [this issue.](https://github.com/gophish/gophish/issues/220)

