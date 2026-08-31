# INC002 - Finance Shared Folder Access

## Overview

Simulated IT support ticket involving a user who was unable to access the Finance shared folder.

**User:** Steve Charlish
**Department:** Finance
**Category:** File & Folder Access
**Priority:** Medium
**Status:** Resolved

## Issue

Steve reported receiving an **Access Denied** error when accessing:

```text
\\SERVER\SharedFolder - Finance
```

The issue was reproduced by testing access while logged in as the affected user.

(images/03-Issue-with-accessing-the-finance-folder.png)

## Investigation

* Verified Steve could successfully log into the domain.
* Checked Steve's Active Directory group membership.
* Reviewed the Finance security group's membership.
* Checked NTFS permissions on the Finance folder.
* Checked the folder's share permissions.

The folder permissions were correctly configured, but Steve was missing from the **Finance security group**.

## Root Cause

Steve was not a member of the security group responsible for granting access to the Finance shared folder.

## Resolution

* Added Steve to the Finance security group.
* Logged out and back into the workstation.
* Confirmed Steve could successfully access the Finance folder.

## Skills Demonstrated

* Active Directory
* Security groups
* NTFS & share permissions
* Windows file sharing
* Troubleshooting and root-cause analysis
* Ticket documentation
* End-user communication

