## opening /etc/fstab
```
sudo nano /etc/fstab
```
## pasteing in /etc/fstab
```
172.20.9.52:/mnt/synopsys /opt/synopsys nfs defaults,soft,timeo=50,retrans=2,_netdev 0 0
```
# .bashrc

## opening .bashrc
```
nano ~/.bashrc
```

## pasting in .bashrc
```
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```

# delete user
```
sudo -i

cd /home

rm -rf ece4

reboot
```
```
sudo userdel -rf ece4
```


# change user
```
sudo -i

useradd -m -s /bin/bash -G wheel ece1

echo "ece1:ece@123" | chpasswd

rm -r /home/ece1

mv /home/ece/* /home/ece1

chown -R ece1:ece1 /home/ece1

reboot
```
