### Summary ###
IJP parses iCalendar formatted text and returns javascript arrays of objects.
[Download it](https://ijp.googlecode.com/svn/trunk/ijp/ijp-0.7.js) - v0.7

### Usage ###
```
icalParser.parseIcal(ical_formatted_text);

//icalParser.icals are now set
icalParser.icals[0].version;
icalParser.icals[0].prodid;

////Arrays of components available
//All the vevent elements
icalParser.icals[0].events;
//All the vtodo elements
icalParser.icals[0].todos;
//All the journal elements
icalParser.icals[0].journals;
//All the freebusy elements
icalParser.icals[0].freebusys;

//Example of a vevent component
var event = icalParser.icals[0].events[0];
event.uid[0]
event.dtstart[0]
event.attendee[0]
event.attendee[1]
event.attendee[2]
event.dtend[0]
etc.

//Each property has at least two fields
event.uid[0].name
event.uid[0].value
//And it can contain a "params" array
event.uid[0].params[parameter_name]

```

### Todo ###

  * Add Timezone elements parsing
  * Add Alarm elements parsing
  * Finish to read RFC 2445 ;P AND 5545