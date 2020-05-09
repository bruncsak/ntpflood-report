# ntpflood-report

There are certain NTP clients which are sendening excessive quantity
of NTP packets, sometimes more than 20k packets per second.

This script reports their IP address into the syslog.

It is possible to set individual report limits per
- second (default: 10000)
- ten seconds (default: 20000)
- minutes (default: 30000)
- ten minutes (default: 40000)
- hour (default: 50000)

Caveats:
The time period is always matches wallclock boundary changes,
and not using sliding time window.
