### To change a static IP address in Ubuntu, follow these steps:

1. Identify the Network Interface

```bash
ip a
```

2. Edit the Netplan Configuration File

```bash
sudo nano /etc/netplan/01-netcfg.yaml
```

3. Modify the Static IP Configuration

```bash
# This file is generated from information provided by the datasource.  Changes
# to it will not persist across an instance reboot.  To disable cloud-init's
# network configuration capabilities, write a file
# /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg with the following:
# network: {config: disabled}
```
```bash
network:
    ethernets:
        enp0s3:
            dhcp4: true
            addresses:
              -  192.168.29.67/28
            routes:
                - to: default
                  via: 192.168.29.1
            nameservers:
               addresses:
                 - 8.8.8.8
                 - 8.8.4.4         
    version: 2
```

4. Apply the Changes

```bash
sudo netplan apply
```

5. Verify the Changes
   To verify that your new static IP has been applied, use the ip a command again

```bash
ip a
```

6. Alternatively, you can check the network connectivity by pinging an external server:

```bash
ping 8.8.8.8
```

```bash
network:
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: false
      addresses:
        - 192.168.29.5/24
      routes:
        - to: default
          via: 192.168.29.1
      nameservers:
        addresses:
          - 8.8.8.8
          - 8.8.4.4
  version: 2
remove 50 cloud init file & create new file and paste above content 

for static ip  (Anuj static ip)
```

