## Things to do after installing Ubuntu 16.04 LTS:

#### Open the terminal (Ctrl+Alt+T) and update + upgrade the system repos:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
#### Install essential tools
```
sudo apt-get install git
sudo apt-get install gksu
```
#### Install useful apps

##### VLC media player (from terminal):
```
sudo apt-get update
sudo apt-get install vlc
```

##### Skype (from terminal)
```
cd ~/Downloads
wget https://repo.skype.com/latest/skypeforlinux-64.deb
sudo dpkg -i skypeforlinux-64.deb
sudo apt install -f
```
Source [https://askubuntu.com/questions/7498/how-do-i-install-skype](https://askubuntu.com/questions/7498/how-do-i-install-skype)

Or alternatively..
```
sudo add-apt-repository "deb http://archive.canonical.com/ $(lsb_release -sc) partner"
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install skype
```
Source [https://idroot.net/linux/install-skype-ubuntu-16-04/](https://idroot.net/linux/install-skype-ubuntu-16-04/)

##### Citrix Receiver

Step 1. Go to the [Citrix receiver for Linux download page](https://www.citrix.com/downloads/citrix-receiver/linux/receiver-for-linux-latest.html) and download the Debian full package. The filename will look like this: icaclient_13.3.0.344519_amd64.deb.

Step 2. Right-click > Open with Software Install > Install. Or alternatively, open and install the package using the Software Center or gdebi.

Step 3. (Now follow steps 5-8 from [https://help.ubuntu.com/community/CitrixICAClientHowTo](https://help.ubuntu.com/community/CitrixICAClientHowTo), namely (from terminal):

Add more SSL certificates
```
sudo ln -s /usr/share/ca-certificates/mozilla/* /opt/Citrix/ICAClient/keystore/cacerts/
sudo c_rehash /opt/Citrix/ICAClient/keystore/cacerts/
```

Configure Citrix Receiver
`/opt/Citrix/ICAClient/util/configmgr &`

(64-bit only) Fix Firefox plugin installation
```
sudo rm -f /usr/lib/mozilla/plugins/npwrapper.npica.so /usr/lib/firefox/plugins/npwrapper.npica.so
sudo rm -f /usr/lib/mozilla/plugins/npica.so
sudo ln -s /opt/Citrix/ICAClient/npica.so /usr/lib/mozilla/plugins/npica.so
sudo ln -s /opt/Citrix/ICAClient/npica.so /usr/lib/firefox-addons/plugins/npica.so
```

Configure Firefox
In Firefox, go to Tools -> Add-ons -> Plugins, and make sure the "Citrix Receiver for Linux" plugin is set to "Always Activate".

Source [https://askubuntu.com/questions/40723/how-do-i-install-citrix-receiver#44137](https://askubuntu.com/questions/40723/how-do-i-install-citrix-receiver#44137)

#### System Settings (left menu bar)
*Appearance > Look* (reduce launcher icon size to 40) > Behaviour (show menus in title bar, select always displayed)
*Brightness & lock >* (never turn off, lock OFF)
*Security & Privacy > Files & Applications* (Record usage OFF, clear usage data, untick all)
*User Accounts >* (tick show my login in the menu bar)

#### Firefox preferences:
Open *Firefox > Preferences*
*General* (Home page [https://duckduckgo.com/](https://duckduckgo.com/))
*Search* (Set default search engine to [https://duckduckgo.com/](https://duckduckgo.com/))
*Privacy & Security > History* (set to Never Remember, clear all history, untick address bar suggestions, Tracking Protection: Always, Untick sending technical data to Firefox)

#### Install printer/scanner driver for SAMSUNG M2070W on Ubuntu 16.04 LTS:

##### 1. Download the driver 
Go to [http://www.samsungdrivers.net/samsung-m2070-driver/](http://www.samsungdrivers.net/samsung-m2070-driver/)
Bottom of the page you'll see *"Samsung M2070 Linux Printer/Scanner Driver Download (15.87 MB)"*

##### 2. Go to your Downloads directory and decompress the downloaded archive:
Right-click > Extract Here
(or in the terminal run: `tar -xvzf ULD_v1.00.29.tar.gz`)

##### 3. Open the terminal (Ctrl+Alt+T) and navigate the uld directory:
```cd Downloads/uld```

##### 4. Run the install-printer.sh file:
`sudo sh ./install-printer.sh` (follow install instructions, `y` to confirm, `Enter` repeatedly to skip through the EULA)

##### 5. Run the install-scanner.sh file:
`sudo sh ./install-scanner.sh`(follow install instructions, `Enter` or `y` to confirm)

##### 6. Connect the printer to your PC and turn it on

##### 7. Open System Settings > Printers > Add > (select Samsung M2070) > Forward > Apply




