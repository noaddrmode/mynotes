# Local Account Installation
```
Shift + F10
OOBE\BYPASSNRO 

Shift + F10
ipconfig /release
```

# Enable long path (long filenames)
```
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" -Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force
```

# dual-boot fix
https://learn.microsoft.com/en-us/windows/release-health/status-windows-11-23h2#3377msgdesc
```
reg add HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecureBoot\SBAT /v OptOut /d 1 /t REG_DWORD
```
