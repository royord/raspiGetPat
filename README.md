# raspiGetPat
0. Enable SSH
0.b set password so that it's not easily hacked.

1. Start by updating expanding filesystem.
raspi-config
expand filesystem

2. After Reboot update the raspberry pi.
sudo apt-get update
sudo apt-get dist-upgrade

3. Install screen and VIM
sudo apt-get install vim screen

Sources:
https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-APRS.pdf
http://www.cantab.net/users/john.wiseman/Documents/ARDOPC.html
http://hamlib.sourceforge.net/manuals/1.2.15/index.html
