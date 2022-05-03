#Okta Identity Cloud Add-on for Splunk

This is an add-on powered by the Splunk Add-on Builder

Download/Install from [splunkbase](https://splunkbase.splunk.com/app/3682/)

03MAY2022
--------

This version is a clone of the 2.25.21 version that exists on Splunkbase as of this writing. 
I have added a single lookup table that providesadditional context to all System Log events, along 
with an automatic lookup. Each event now contains a series of tags, a plain-text description,
and a categorization of "security" or "admin" interest. This additional data comes from the 
System Log API documentation at the URL below:

https://developer.okta.com/docs/reference/api/event-types/

A dashboard is also provided to investigate this newly enriched data.

Specifically, an automated lookup adds the following fields to the sourcetype OktaIM2:log:

admin_interest: Events that should be of interest to Okta administrators (boolean)
security_interest: Events that should be of interest to security audiences, e.g. SOC or operations (boolean)
event_type_description: Plain-text description of event, pulled from URL above (string)
event_type_tags: Event type tags in pipe-delimited format, pulled from URL above (string)
release_note_date: Date that this event was released in the System Log API, pulled from URL above (string)
smushed_event_type: Not terribly useful, actually...

The dashboard "Admin & Security Log Explorer" is provided as an example way to leverage this data. 
It allows slicing-and-dicing of System Log data based on the Admin, Security, and Tag enrichments mentioned above.

James Brodsky
james.brodsky@okta.com

