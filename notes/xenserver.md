# basics
```
xe sr-list  # uuid=1ccf3367-4d99-85db-ea72-9945095c8112
xe vm-list
xe vm-shutdown uuid=<hash> force=true
xe vm-start uuid=<hash>
xe vm-list params=name-label,power-state,networks
```

# auto-restart pool
```
xe pool-list
xe pool-param-list uuid=2fdf2df2-8cab-6fb3-2c57-5ae8686d918f
xe pool-param-set uuid=2fdf2df2-8cab-6fb3-2c57-5ae8686d918f other-config:auto_poweron=true
```

# auto-restart VM
```
xe vm-list
xe vm-param-set uuid=4f8038ef-380e-6499-e696-32bded3d4edb other-config:auto_poweron=true
xe vm-param-list uuid=4f8038ef-380e-6499-e696-32bded3d4edb
```

# iso repo
```
cd /opt/iso-images/
cd /var/run/sr-mount/1ccf3367-4d99-85db-ea72-9945095c8112/iso-images/
wget ubuntu.iso
xe sr-create name-label=local-iso-2 type=iso device-config:location=/var/run/sr-mount/1ccf3367-4d99-85db-ea72-9945095c8112/iso-images device-config:legacy_mode=true content-type=iso
```

