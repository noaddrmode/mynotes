# Example config
Make sure to delete ~/.cert/  
Also debian has a bug with password, so this config is necessary.
```
cert-pass-flags=0

[vpn-secrets]
cert-pass=mypassword
```

```
sudo systemctl restart NetworkManager.service
sudo usermod -aG systemd-journal <username>
journalctl -f

# /etc/NetworkManager/system-connections/test.nmconnection
[connection]
id=myvpn
uuid=99385800-e1f4-4adc-a21a-d66bc0ca89cf
type=vpn
autoconnect=false

[vpn]
ca=/home/test/.cert/nm-openvpn/ca.pem
cert=/home/test/.cert/nm-openvpn/cert.pem
cert-pass-flags=0
connection-type=tls
dev=tun
float=yes
key=/home/test/.cert/nm-openvpn/cert.key
remote=192.168.33.1:1194
service-type=org.freedesktop.NetworkManager.openvpn

[vpn-secrets]
cert-pass=mypassword

[ipv4]
method=auto

[ipv6]
addr-gen-mode=stable-privacy
method=auto

[proxy]
```
