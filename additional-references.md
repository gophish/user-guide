# Additional References

## Community Guides

\*\*\*\*[**Simulated Phishing Educational Guide**](http://tinyurl.com/PhishCampaign)  
****Author: [LarryGrim](https://github.com/LarryGrim)

\*\*\*\*[**Practical Phishing with Gophish**](https://medium.com/airwalk/practical-phishing-with-gophish-7dd384ad1840)  
Author: [Jim Lamb](https://twitter.com/ovineOppressor)

\*\*\*\*[**Conducting USB Drop Tests With GoPhish**](https://medium.com/@chrismerkel/conducting-usb-drop-tests-with-gophish-44cc7e1a88b9)  
Author: [Chris Merkel](https://twitter.com/chrismerkel)

## Tools

\*\*\*\*[**GoReport**](https://github.com/chrismaddalena/GoReport)  
****Author: [Chris Maddalena](https://twitter.com/cmaddalena)  
_A Python script to collect campaign data from Gophish and generate a report_

\*\*\*\*[**Phishbuckets**](https://github.com/CommArc/phishbuckets)  
****Author: [snori74](https://github.com/snori74)  
_Command-line scripts to manage phishing campaigns with API calls to a Gophish server_

\*\*\*\*[**Lure**](https://github.com/highmeh/lure)  
****Author: [Jayme \(highmeh\)](https://twitter.com/highmeh)  
_Lure assists in phishing target collection by pulling and parsing email addresses for a target organization. The results are normalized into a format recognized by Gophish, and then uploaded to the server._


## Reporting: Results and Raw Event date/time format

****Author: [Luke-Tech](https://github.com/Luke-Tech)  
_When reporting a campaing, you may prefer a more human readable date and/or time format. The following formulas are useful in Excel or LibreOffice_

`=TEXT(DATEVALUE(MID(B2,6,2)&"/"&MID(B2,9,2)&"/"&MID(B2,1,4))+(TIMEVALUE(MID(B2,12,2)&":"&MID(B2,15,2)&":"&MID(B2,18,2))+1-TIME(5,0,0)),"mm/dd/yyyy h:mm:ss AM/PM")`
Formats to **"mm/dd/yyyy hh:mm:ss AM/PM."**

`=TEXT(DATEVALUE(MID(B2,6,2)&"/"&MID(B2,9,2)&"/"&MID(B2,1,4)),"mm/dd/yyyy")`
Formats to **"mm/dd/yyyy"** if you want only the date.

`=TEXT(TIMEVALUE(MID(B2,12,2)&":"&MID(B2,15,2)&":"&MID(B2,18,2))+1-TIME(5,0,0),"h:mm:ss AM/PM")`
Formats to **"hh:mm:ss AM/PM."** if you want only the time.

Place any of these into a new column, starting at row 2, then fill down. Modify references to B2 if the existing date/time format appears elsewhere. The Events.csv output file uses column B by default, and no change is necessary to the formulas. The Results.csv output file uses columns F and H. Adjust accordingly.

The time zone is preset for United States EST (GMT -5). Modify the formula to your needs: _"-TIME(H,M,S)"_ where H sets the offset from GMT/zulu time in hours. 5 is the offset for EST, 6 is equivalent to EDT or CST. Similar where M sets the minutes offset.
