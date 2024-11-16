# ntpflood-report

There are certain NTP clients that are sending excessive quantity
of NTP packets, sometimes more than 20k packets per second.

This script reports their IP address into the syslog.
When started, it becomes a background job.
In verbose or higher level debug mode the program will not go into the background
and it prints its output instead of logging into the syslog.

There are preset individual report limits per
- second
- ten seconds
- minutes
- ten minutes
- hour

If you want to change these values, just customize the code for your need.

Every IP address is reported no more than once an hour.

Caveats:
The time period is always matches wallclock boundary changes,
and not using sliding time window.

You may want to start first in debugging mode with the options:
-d 2 -p 20
