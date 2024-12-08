# Virtualbox host-only adpater (deprecated) fix on MAC OS
Enable port forwarding on NAT Network
- Settings -> Network -> Choose (NAT) in adapter -> Port forwarding
- Use Protocol (TCP), Host IP (127.0.0.1), Host Port (2222), Guest IP (0.0.0.0), Guest Port (22)
- Then, use `ssh user@127.0.0.1 -p 2222` from host to login to VM
