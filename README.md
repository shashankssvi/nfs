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
# Synopsys License
export SNPSLMD_LICENSE_FILE=27020@14.139.1.126

export SYNOPSYS_INSTALLED_FILES="/opt/synopsys/synopsys_installed_tools"

export CUSTOM_COMPILER="$SYNOPSYS_INSTALLED_FILES/customcompiler/V-2023.12"
export CUSTOM_INFRASTRUCTURE="$SYNOPSYS_INSTALLED_FILES/custominfrastructure/V-2023.12"
export PRIME_WAVE="$SYNOPSYS_INSTALLED_FILES/primewave/V-2023.12"
export HSPICE="$SYNOPSYS_INSTALLED_FILES/hspice/X-2025.06-SP1-2/hspice"
export HSIMPLUS="$SYNOPSYS_INSTALLED_FILES/hsim/U-2023.03/hsimplus"
export PRIMESIM_HOME="$SYNOPSYS_INSTALLED_FILES/primesim/X-2025.06-SP1-2"
export ICVALIDATOR="$SYNOPSYS_INSTALLED_FILES/icvalidator/U-2022.12-SP2"
export WAVE_VIEW="$SYNOPSYS_INSTALLED_FILES/wv/W-2024.09-SP2-2"
export SPYGLASS="$SYNOPSYS_INSTALLED_FILES/spyglass/U-2023.03-SP2/SPYGLASS_HOME"
export VCS_HOME="$SYNOPSYS_INSTALLED_FILES/vcs/U-2023.03"
export VERDI_HOME="$SYNOPSYS_INSTALLED_FILES/verdi/U-2023.03-SP1"
export STARRC="$SYNOPSYS_INSTALLED_FILES/starrc/W-2024.09-SP2"
export SYN="$SYNOPSYS_INSTALLED_FILES/syn/W-2024.09-SP5-5"
export ICC2="$SYNOPSYS_INSTALLED_FILES/icc2/U-2022.12-SP3"
export NT="$SYNOPSYS_INSTALLED_FILES/nt/W-2024.09-SP5"
export PPOWER="$SYNOPSYS_INSTALLED_FILES/prime/W-2024.09-SP5-2"
export PRIMETIME="$SYNOPSYS_INSTALLED_FILES/pt_vW-2024.09-SP5/prime/W-2024.09-SP5-2"
export TEXTMAX="$SYNOPSYS_INSTALLED_FILES/testmax/U-2022.12-SP3"

# Add Synopsys tools to PATH
export PATH=$PRIMESIM_HOME/bin:$ICC2/bin:$TEXTMAX/bin:$NT/bin:$PPOWER/bin:$HSIMPLUS/bin:$PRIMETIME/bin:$VCS_HOME/bin:$CUSTOM_COMPILER/bin:$CUSTOM_INFRASTRUCTURE/bin:$VERDI_HOME/bin:$SYN/bin:$HSPICE/bin:$PRIME_WAVE/bin:$ICVALIDATOR/bin:$STARRC/bin:$WAVE_VIEW/bin:$SPYGLASS/bin:$PATH:/usr/X11R6/bin:/usr/bin:/bin

export FLEXLM_DIAGNOSTICS=3
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```

# install 
```
sudo dnf install -y tcsh ksh redhat-lsb gcc gcc-c++ make \
libX11 libXext libXt libXft libXScrnSaver libXrender \
libnsl elfutils-libelf glibc-devel ncurses-compat-libs \
fontconfig freetype libpng libjpeg-turbo
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
