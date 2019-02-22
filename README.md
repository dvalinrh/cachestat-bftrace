# cachestat.bt

cachestat.bt is a bpftrace script that retrieces from the kernel the pagecache miss and hits.  It will print to the terminal at a designated interval the number of hits and misses during the interval, percentage of hits and a time stamp.

Usage
./cachestat.bt <interval in seconds> <nmber of intervals to present>
  <interval in seconds>:  Is the time period in seconds for gathering the cache hits and miss, default is 5 seconds.
  <number of intervals to present>: How many time intervals to present.  Only meaningful when <interval in seconds> is designated. 
  The default is to run forever.
                                            
# ./cachestat.bt 5 10

Attaching 7 probes...

        Hits      Misses       %hits
      272275       68302          79% 09:29:27
      238210       60501          79% 09:29:33
      260234       67884          79% 09:29:39
      280268       70056          80% 09:29:45
      257868       66952          79% 09:29:51
      241025       60734          79% 09:29:57
      266305       68233          79% 09:30:03
      268565       69923          79% 09:30:09
      265550       69093          79% 09:30:15
      237310       62154          79% 09:30:21

Summary

total hits:      2587612

total miss:       663832

Hit percentage           79

