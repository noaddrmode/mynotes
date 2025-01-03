# nmcli 
```
$ nmcli -f name,device,type,filename con show
NAME    DEVICE  TYPE      FILENAME
enp0s3  enp0s3  ethernet  /etc/NetworkManager/system-connections/enp0s3.nmconnection
enp0s8  enp0s8  ethernet  /etc/NetworkManager/system-connections/enp0s8.nmconnection
lo      lo      loopback  /run/NetworkManager/system-connections/lo.nmconnection

$ nmcli device show enp0s3
GENERAL.DEVICE:                         enp0s3
GENERAL.TYPE:                           ethernet
GENERAL.HWADDR:                         08:00:27:23:2F:2E
GENERAL.MTU:                            1500
GENERAL.STATE:                          100 (connected)
GENERAL.CONNECTION:                     enp0s3
GENERAL.CON-PATH:                       /org/freedesktop/NetworkManager/ActiveConnection/2
WIRED-PROPERTIES.CARRIER:               on
IP4.ADDRESS[1]:                         10.0.2.15/24
IP4.GATEWAY:                            10.0.2.2
IP4.ROUTE[1]:                           dst = 10.0.2.0/24, nh = 0.0.0.0, mt = 100
IP4.ROUTE[2]:                           dst = 0.0.0.0/0, nh = 10.0.2.2, mt = 100
IP4.DNS[1]:                             10.0.2.3
IP6.ADDRESS[1]:                         fd00::a00:27ff:fe23:2f2e/64
IP6.ADDRESS[2]:                         fe80::a00:27ff:fe23:2f2e/64
IP6.GATEWAY:                            fe80::2
IP6.ROUTE[1]:                           dst = fe80::/64, nh = ::, mt = 1024
IP6.ROUTE[2]:                           dst = fd00::/64, nh = ::, mt = 100
IP6.ROUTE[3]:                           dst = ::/0, nh = fe80::2, mt = 100

$ cat /etc/NetworkManager/system-connections/enp0s3.nmconnection
https://networkmanager.dev/docs/api/latest/settings-ipv4.html

$ nmcli connection modify enp0s3 \
ipv4.method "manual" \
ipv4.addresses "192.168.56.101/24" \
ipv4.gateway "192.168.56.1" \
ipv4.dns "192.168.56.1,1.1.1.1"
```
