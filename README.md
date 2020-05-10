# ntpflood-report

There are certain NTP clients that are sending excessive quantity
of NTP packets, sometimes more than 20k packets per second.

This script reports their IP address into the syslog.

There are preset individual report limits per
- second (10000)
- ten seconds (20000)
- minutes (30000)
- ten minutes (40000)
- hour (50000)

If you want to change these values, just customize the code for your need.

Every IP address is reported no more than once an hour.

Caveats:
The time period is always matches wallclock boundary changes,
and not using sliding time window.
