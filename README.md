## open /etc/fstab
```
sudo nano /etc/fstab
```
## line to be added in /etc/fstab
```
172.20.9.52:/home/install  /opt/synopsys  nfs  _netdev,nofail,x-systemd.automount,timeo=10,retrans=1,retry=0  0  0
172.20.9.189:/home/install  /home/install  nfs  _netdev,nofail,x-systemd.automount,timeo=10,retrans=1,retry=0  0  0
```
## Mount cmd
```
sudo mkdir -p /home/install
sudo systemctl daemon-reload
sudo mount /home/install
```
## To mount the nfs systems
```
sudo mount -a
sudo mount cadance
sudo mount synopsys
```

## Run cadence tool
```
csh
source /home/install/cshrc
```

## Run synopsis tool
```
source /home/synopsys/synopsys.bashrc
```
