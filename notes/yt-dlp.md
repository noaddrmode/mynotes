# m3u8
```
./yt-dlp \
  -f 0 \
  --user-agent "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.5112.79 Safari/537.36" \
  --hls-prefer-native \
  https://127.0.0.1/example.m3u8
```

# cookie
```
./yt-dlp \
  -f 'bestvideo[height<=1280]+bestaudio' \
  --cookies-from-browser firefox:/mnt/c/Users/username/AppData/Roaming/Mozilla/Firefox/Profiles/abcdefgh.default-release \
  https://127.0.0.1
```
