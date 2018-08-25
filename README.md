# raspiGetPat
0. Enable SSH
0.b set password so that it's not easily hacked.

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

Left off with issue installing hamlib, will need to pick it up here.

###Sources:
https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-APRS.pdf
install of hamlib falls short on the pdf document above:
http://hamlib.sourceforge.net/manuals/1.2.15/_i_n_s_t_a_l_l.html

http://www.cantab.net/users/john.wiseman/Documents/ARDOPC.html
http://hamlib.sourceforge.net/manuals/1.2.15/index.html
