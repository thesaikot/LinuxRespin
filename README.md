# LinuxRespin
Fork of remastersys - updates

This tool is used to backup your image, create distributions, create live cd/dvds.
install respin

If you are using Ubuntu - you need to install xresprobe. There are debs in the Ubuntu folder. Alternately:

wget http://security.ubuntu.com/ubuntu/pool/universe/x/xresprobe/xresprobe_0.4.24ubuntu9_amd64.deb
dpkg -i xresprobe_*ubuntu9_amd64.deb
apt-get install -y dialog casper libdebian-installer4 ubiquity-frontend-debconf user-setup discover
apt-get -fy install
git clone https://github.com/ch1x0r/LinuxRespin.git
dpkg -i LinuxRespin/ubuntu/respin_1.1.0-1_all.deb

To uninstall, run:
sudo apt-get remove respin
or sudo apt-get purge respin 
(if you are using sudo)

There is a gui available. I will post this soon. 
Using the gui, you can change the boot screen. 

Remember, if you are creating a distro for public use, to use your own trademarked icons for the menu, etc. 
You can change these easily by researching the process for your particular base. 
You can change the plymouth theme also.

Maintaining a distro is important. 
Remember to build a community around your distro if that is what you want.
Customizing and creating distro can be fun and challenging. Also, this is a great way to learn more about distros and GNU Linux!




