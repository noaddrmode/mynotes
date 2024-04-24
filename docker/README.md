# Usage
Build an image
```
docker build -t mytag -f Dockerfile-openwrt .
```
Run services
```
docker compose -f Dockercompose-influxdb up -d
```