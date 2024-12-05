# Alma Linux
https://wiki.almalinux.org/series/system/SystemSeriesA02.html  

```
$ sudo firewall-cmd --list-all
public (active)
  target: default
  icmp-block-inversion: no
  interfaces: enp0s3 enp0s8
  sources:
  services: cockpit dhcpv6-client ssh
  ports: 8000/tcp 3000/tcp
  protocols:
  forward: yes
  masquerade: no
  forward-ports:
  source-ports:
  icmp-blocks:
  rich rules:

$ sudo firewall-cmd --get-default-zone
public

$ sudo firewall-cmd --list-services
cockpit dhcpv6-client ssh

$ sudo firewall-cmd --list-ports
3000/tcp 8000/tcp

$ sudo firewall-cmd --add-port=8080/tcp
$ sudo firewall-cmd --list-all
ports: 8000/tcp 3000/tcp 8080/tcp
$ sudo firewall-cmd --reload
 ports: 8000/tcp 3000/tcp
$ sudo firewall-cmd --add-port=8080/tcp --permanent
$ sudo firewall-cmd --reload
ports: 8000/tcp 3000/tcp 8080/tcp
$ sudo firewall-cmd --remove-port=8080/tcp --permanent
```

