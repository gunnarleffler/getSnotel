getSnotel v2.3.0

17 July 2017

Author: Gunnar Leffler

PURPOSE:
========
This utility queries SNOTEL data from the NRCS web service and outputs SHEF.

USAGE:
======

REALTIME:
---------
`getSnotel <NRCS Snotel ID> <state code> <local station id> <SHEF physical element codes> <Query Days>`

DAILY:
------
`getSnotel daily <NRCS Snotel ID> <state code> <local station id> <SHEF physical element codes> <Query Days>`

The SHEF PE codes can be in any order. Codes currently supported:
*  SW - Snow Water Equivalent
*  SD - Snow Depth
*  PC - Accumulated Precipitation to Date
*  TA - Current Air Temperature
*  TM - Average Temperature
*  TX - Maximum Temperature
*  TN - Minimum Temperature

output is piped to Standard Out (STDOUT).

METADATA:
---------
`getSnotel metadata <NRCS Snotel ID> <state code> <type>`

This returns metadata about a requested snotel station in JSON format

`getSnotel reservior <NRCS Snotel ID> <state code> <type>`

This returns metadata about a requested reservoir in JSON format

FORECAST:
---------
getSnotel forecast <NRCS Snotel ID> <station id> <local station id> <physical element codes> <Query Days>

EXAMPLES:
=========
    REALTIME : getSnotel 302 OR ANRO SWSDPCTATMTXTN 3days
    DAILY    : getSnotel daily 302 OR ANRO SWSDPCTATMTXTN 3days
    METADATA : getSnotel metadata 304 OR SNTL
    RESERVOIR: getSnotel reservoir 06641500 WY BOR
    FORECAST : getSnotel forecast 14362000 OR APLO SRVO APR-JUL 90DAYS

