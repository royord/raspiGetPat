# raspiGetPat
0. Enable SSH
0.b set password so that it's not easily hacked.

1. Start by updating expanding filesystem.
<code>
  sudo raspi-config
  </code>
expand filesystem

2. After Reboot update the raspberry pi.
<code>
sudo apt-get update
sudo apt-get dist-upgrade
</code>

3. Install screen and VIM
<code>
sudo apt-get install vim screen
</code>

4. Install hamlib
<code>
sudo apt-get install automake libtool textinfo<br>
cd ~<br>
git clone git://hamlib.git.sourceforge.net/gitroot/hamlib/hamlib<br>
cd hamlib<br>
sh autogen.sh<br>
make<br>
make check<br> 
sudo make install<br>
</code>

Sources:
https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-APRS.pdf
http://www.cantab.net/users/john.wiseman/Documents/ARDOPC.html
http://hamlib.sourceforge.net/manuals/1.2.15/index.html
