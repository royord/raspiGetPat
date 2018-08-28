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
sudo apt-get install vim screen git -y
```
3a. Start Screen
```
screen
```

4. Install hamlib
```
sudo apt-get install libhamlib-utils
```

5. Install alsa shield
```
sudo apt-get install libasound2 libasound2-dev
```
6. Download/Install piardopc
```
wget http://www.cantab.net/users/john.wiseman/Downloads/Beta/piardopc
```
7. Install Direwolf
```
cd ~
git clone https://www.github.com/wb2osz/direwolf
cd direwolf
make
sudo make install
make install-conf
```
8. Install GO language
```
sudo apt-get install golang
```
9. Add the following lines to ~/.bashrc, reboot after.
```
export GOPATH=$HOME/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
```
10. Install PAT from getpat.io as suggensted with the following command. Please note that this may take some time please be patient with the install.
```
go get github.com/la5nta/pat
```
11. Configure pat by running `pat configure` make sure to set the following:
```
"mycall":<yourCallsign>
"secure_login_password":<yourSecretPassword>
```
If you plan to use the web interface you may want to also change 
```
"http_addr": "localhost:8080",
```
to
```
"http_addr": "0.0.0.0:8080",
```
so that you can use pat from any connected device.
Left off with issue installing hamlib, will need to pick it up here.
- Installing Direwolf
- Installing PAT
- Running needed components as a service.
- on the KX3 you will need to set the baud rate to get a solid connection to the radio using rigctl

Commands that may be useful, need to document how to work with these commands.
'''
arecord -l
aplay -l
./piardopc 8515 hw:1,0 hw:1,0 -c /dev/ttyUSB0 -- working command
'''

### Sources:
https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-APRS.pdf

install of hamlib falls short on the pdf document above:

http://hamlib.sourceforge.net/manuals/1.2.15/_i_n_s_t_a_l_l.html

http://www.cantab.net/users/john.wiseman/Documents/ARDOPC.html
http://hamlib.sourceforge.net/manuals/1.2.15/index.html
