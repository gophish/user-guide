# Importing Groups

The first thing we need to do before we can launch a campaign is to figure out who to target. There are a ton of ways to gather/generate email addresses for potential targets. You can either harvest email addresses from public information using OSINT if you are aiming to simulate a realistic scenario.

Now that we have our list of users, let’s import them into gophish.

To add a group, navigate to the “Users & Groups” page and click “New Group”:

![New Group Modal](https://i.imgur.com/kBZdT0G.png)

Since we are performing phishing simulation for Morning Catch, we can call our group “Morning Catch Employees”.

Now we have to add the members. There are two ways to do this:

* Add each member’s details one at a time using the form inputs
* Bulk import the group from a CSV file

To save time \(and typing!\) let’s go with the CSV option.

## Importing from CSV

The CSV format gophish expects has the following header values:

* First Name
* Last Name
* Email
* Position

So, the CSV for Morning Catch would look like the following:

```text
First Name,Last Name,Email,Position
Richard,Bourne,rbourne@morningcatch.ph,CEO
Boyd,Jenius,bjenius@morningcatch.ph,Systems Administrator
Haiti,Moreo,hmoreo@morningcatch.ph,Sales & Marketing
```

After uploading this CSV using the “Bulk Import Users” button, we see that our members were added automatically:

![Importing users](http://imgur.com/58fvRZ3.png)

After clicking “Save changes”, we see a confirmation message that our group was created.

> Tip: If you don’t see the group show up right away, refresh the page and it should appear in the table.

