# view open ports
```
lsof -Pi | grep -i listen
```

# don't extract zip contents on double-click
Finder -> Mac > System > Library > Core Services > Applications > Archive Utility.app > Open > Settings > Uncheck "Keep expanding as possible"

# allow unknown app
```
xattr -dr com.apple.quarantine /Applications/peazip.app
```
