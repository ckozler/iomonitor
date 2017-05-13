# iomonitor
Wrapper script for ioping that can work with nagios or standalone to measure storage latency of a directory/disk/mount

Example usage:

./iomonitor --directory /tmp --min-warn 0 --min-crit 0 --max-warn 0 --max-crit 0 --avg-warn 0 --avg-crit 0 --count 15

And of course, modify warn/crit values for minimum, maximum, and average accordingly

It is suggested to first get a baseline for what your system looks like by
running the script with all zeros for crit/warn then using "raw data" line 
to generate some  values you consider warn/critical. I used a 
count of 120 (2 minutes) then min/max/avg * 1.5 for warning and * 2.5 for critical
