getSnotel v2.1
13 June 2013
Gunnar Leffler

PURPOSE:
--------
This utility queries SNOTEL data from the NRCS web service and outputs SHEF.

USAGE:
------
REALTIME:
getSnotel <NRCS Snotel ID> <state code> <local station id> <SHEF physical element codes> <Query Days>

DAILY:
getSnotel daily <NRCS Snotel ID> <state code> <local station id> <SHEF physical element codes> <Query Days>

The SHEF PE codes can be in any order. Codes currently supported:
  SW - Snow Water Equivalent
  SD - Snow Depth
  PC - Accumulated Precipitation to Date
  TA - Current Air Temperature
  TX - Maximum Temperature
  TN - Minimum Temperature

output is piped to Standard Out (STDOUT).

METADATA:
getSnotel metadata <NRCS Snotel ID> <state code> <type>

This returns metadata bout a requested snotel station in JSON format

EXAMPLES:
---------
REALTIME: getSnotel 302 OR ANRO SWSDPCTATXTN 3days
DAILY   : getSnotel 302 OR ANRO SWSDPCTATXTN 3days
METADATA: getSnotel metadata 304 OR SNTL
