# raspiGetPat
0. Enable SSH by placing a 'ssh' file in the 'boot' drive before starting up the raspberry pi for the first time. This can be done after the flashing has been done by either mounting '/dev/sdX1' and running `touch ssh` within the directory. From a mac you can use `touch /Volumes/boot/ssh`, providing that the boot volume is mounted.

0.b set password so that it's not easily hacked.
```
passwd
```
1. Start by updating expanding filesystem.
```
  sudo raspi-config
```
expand filesystem

2. After Reboot update the raspberry pi.
```
sudo apt-get update
sudo apt-get dist-upgrade -y
```

3. Install screen and VIM
```
sudo apt-get install vim screen
```
3a. Start Screen
```
  screen
```
..b. Install Git

`sudo apt-get install git -y`

4. Install hamlib
```
sudo apt-get install automake libtool textinfo
cd ~
git clone git://hamlib.git.sourceforge.net/gitroot/hamlib/hamlib
cd hamlib
sh autogen.sh
make
make check
sudo make install
```
Purposed install method:
```
./configure
make
sudo make install
```

Left off with issue installing hamlib, will need to pick it up here.
Installing PAT
Installing piardopc

###Sources:
https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-APRS.pdf

install of hamlib falls short on the pdf document above:

http://hamlib.sourceforge.net/manuals/1.2.15/_i_n_s_t_a_l_l.html

http://www.cantab.net/users/john.wiseman/Documents/ARDOPC.html
http://hamlib.sourceforge.net/manuals/1.2.15/index.html
