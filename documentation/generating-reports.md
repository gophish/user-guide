# Generating Reports

Reporting is an important part of any Gophish campaign. To help facilitate generating reports, there are a few options you could consider:

## Using the Web UI

The Gophish dashboard gives a quick overview showing the results for a particular campaign:

![](../.gitbook/assets/localhost_3333_campaigns_25-macbook.png)

In addition to providing the results in the dashboard, you have the option to export the raw logs from Gophish using the "Export CSV" button at the top of the page. You could then parse these CSV files using other software such as Excel or Google Sheets.

## Using GoReport

Gophish has an incredible community that has built tools around the API to help make reporting easy. A great example of this is called [GoReport](https://github.com/chrismaddalena/GoReport).

[GoReport](https://github.com/chrismaddalena/GoReport), created by Github user [@chrismaddalena](https://github.com/chrismaddalena/), provides a really simple, clean way to generate reports for a given Gophish campaign. You can use this script to generate reports for the campaign in either CSV or DOCX format.

## Leveraging the API

If you are wanting to make custom reports, perhaps for one or more campaigns, we strongly suggest you consider leveraging the extensive [Gophish API](https://docs.getgophish.com/api-documentation/).

We have a [Python API client](https://github.com/gophish/api-client-python) that can help facilitate getting the data you need from the API. You can find the documentation for the Python API client [here](https://docs.getgophish.com/python-api-client/).

