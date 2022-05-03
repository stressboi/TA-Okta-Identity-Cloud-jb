#Okta Identity Cloud Add-on for Splunk

This is an add-on powered by the Splunk Add-on Builder

Download/Install from [splunkbase](https://splunkbase.splunk.com/app/3682/)

5-3-2022
--------

This version is a clone of the 2.25.21 version that exists on Splunkbase as of this writing. I have added a single lookup table that provides
additional context to all System Log events, along with an automatic lookup. Each event now contains a series of tags, a plain-text description,
and a categorization of "security" or "admin" interest.

A dashboard is also provided to investigate this newly enriched data.

James Brodsky
james.brodsky@okta.com
03MAY2022
