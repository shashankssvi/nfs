## open /etc/fstab
```
sudo nano /etc/fstab
```
## line to be added in /etc/fstab
```
172.20.9.149:/home/install  /home/install  nfs  _netdev,nofail,x-systemd.automount,timeo=10,retrans=1,retry=0  0  0
```
## Mount cmd
```
sudo mkdir -p /home/install
sudo systemctl daemon-reload
sudo mount /home/install
```
