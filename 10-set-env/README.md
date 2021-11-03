---
id: README
title: README
date: 2021-11-03 00:27:04
---

## 1. set `git` env

	add to path: F:\Program Files\Git\cmd

## 2. How to save the old PATH and get them after new Windows installing

I saved the old PATH to: `F:\OneDrive\super\env-vars.clixml`

```powershell title="PowerShell"
# Save all the process' environment variables in CLIXML format.
Get-ChildItem env: | Export-CliXml ./env-vars.clixml

# ... modify the env. variables

# Restore the previously saved env. variables.
Import-CliXml ./env-vars.clixml | % { Set-Item "env:$($_.Name)" $_.Value }
```
