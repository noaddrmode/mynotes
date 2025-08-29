# Find files
```
Get-ChildItem -File -recurse -Include *myname* 
find . -name '*myname*'
```

# Rename files
```
mkdir tmp && cd tmp
ls ../*.mp4 | while read filename; do new=$(echo "$filename" | grep -o 'p[0-9]\+ ' | xargs); cp "$filename" "$new.mp4"; done
```

# Chrome custom profile
chrome.exe --user-data-dir=c:\foo

# Firefox custom profile
firefox.exe -P foo -no-remote

# Firefox reuse old profile
firefox -allow-downgrade    
Delete C:\Users\vm\AppData\Roaming\Mozilla\Firefox\Profiles\xxxxx.default-release\compatibility.ini    
or change `LastVersion`
```
[Compatibility]
LastVersion=136.0.4_20250326231000/20250326231000
LastOSABI=WINNT_x86_64-msvc
LastPlatformDir=C:\Users\vm\AppData\Local\Mozilla Firefox
LastAppDir=C:\Users\vm\AppData\Local\Mozilla Firefox\browser
```

# Firefox about:config
```
# https://support.mozilla.org/en-US/kb/how-stop-firefox-making-automatic-connections
browser.compactmode.show : true
browser.cache.disk.enable : false
browser.download.start_downloads_in_tmp_dir : true
dom.event.contextmenu.enabled : false
dom.popup_allowed_events : dblclick
dom.popup_maximum : 0
geo.enabled : false
network.prefetch-next : false
network.captive-portal-service.enabled : false
network.connectivity-service.enabled : false
media.autoplay.blocking_policy : 1     # 1 or 2 https://wiki.mozilla.org/Media/block-autoplay
browser.urlbar.maxRichResults: 8
```

# ublock filter
```
no-popups: * true
```
