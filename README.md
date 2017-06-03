Disclaimer
==========
As always, do not use anything for malicious intent.

Code written by Vincent Yiu of ActiveBreach by MDSec Consulting Ltd (www.mdsec.co.uk)

Description
===========

Invoke-DNSDiscovery scans a list of common names that could be used to identify interesting assets on an internal network / Windows domain. This script is useful for performing internal DNS reconnaisance after breaching the perimeter.

Usage
=====

Brute force common names embedded in the script for a full DNS path and export to CSV

```
PS C:\> Invoke-DNSDiscovery -Path dns.csv
[*] Using default names list
[*] Number of names: 20015
[*] All names requested, waiting for completion
[*] Written the results to dns.csv
[*] Module Completed
```

Use a supplied name list that may be shorter.

```
PS C:\> Invoke-DNSDiscovery -Namelist names.txt -Path dns_short.csv
[*] Using names.txt
[*] Number of names: 4
[*] All names requested, waiting for completion
[*] Written the results to dns_short.csv
[*] Module Completed
```