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
