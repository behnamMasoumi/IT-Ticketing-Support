# INC003 - Internal HR Website Unavailable

## Overview

Simulated IT support ticket involving a user who was unable to access the company's internal HR website.

**User:** Sarah
**Department:** HR
**Category:** DNS / Website Access
**Priority:** Medium
**Status:** Resolved

## Issue

Sarah reported that she could not access:

```text
http://hr.ben.local
```

![User unable to access the internal website](images/04%20-%20Unable%20to%20access%20the%20internal%20website%20using%20the%20domain%20name.png)

## Investigation

* Confirmed `hr.ben.local` did not resolve through DNS.
* Verified the website was reachable directly by IP address.
* Identified that the `hr` DNS record was missing from the `ben.local` DNS zone.

## Resolution

* Recreated the `hr` DNS record.
* Flushed the client's DNS cache.
* Verified DNS resolution with `nslookup`.
* Confirmed the HR website loaded successfully.

![HR dns record added to the domain](images/06%20-%20Adding%20the%20HR%20DNS%20record%20to%20ben.local.png)
![Flushing the DNS - Testing using nslookup](images/07%20-%20nslookup%20the%20domain%20name%20after%20flushing%20the%20dns.png)
![Website is now loading successfully](images/08%20-%20Verifying%20the%20DNS%20resolution%20works%20properly.png)

## Skills Demonstrated

* Windows Server DNS
* DNS record management
* DNS troubleshooting
* `nslookup`
* `ipconfig /flushdns`
* Root-cause analysis
* Ticket documentation
