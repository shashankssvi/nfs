## open /etc/fstab
```
sudo nano /etc/fstab
```
## line to be added in /etc/fstab
```
172.20.9.52:/home/synopsys  /home/synopsys  nfs  _netdev,nofail,x-systemd.automount,timeo=10,retrans=1,retry=0  0  0
172.20.9.189:/home/install  /home/install  nfs  _netdev,nofail,x-systemd.automount,timeo=10,retrans=1,retry=0  0  0
```

## Mount cmd
```
sudo mkdir -p /home/install
sudo mkdir -p /home/synopsys
sudo systemctl daemon-reload
```
## To mount the nfs systems
> All at once
```
sudo mount -a
```
> One at a time
```
sudo mount /home/install
sudo mount /home/synopsys
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
