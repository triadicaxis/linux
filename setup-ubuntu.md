---
output:
 pdf_document: default
 html_document: default
---
## Things to do after installing Ubuntu 16.04 LTS:

#### Open the terminal (Ctrl+Alt+T) and update + upgrade the system repos:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
#### Install some basic tools

```
sudo apt-get install git
sudo apt-get install gksu
sudo apt-get update && sudo apt-get install pandoc
``` 

#### Install useful apps

Also see [http://www.linuxandubuntu.com/home/50-essential-linux-applications](http://www.linuxandubuntu.com/home/50-essential-linux-applications) 
Also see [https://www.youtube.com/watch?v=a5cvg9XKEL8](https://www.youtube.com/watch?v=a5cvg9XKEL8)

* rambox
* kodi
* stacer
* timeshift
* kdenlive
* synaptic
* vlc
* nitroshare
* chromium
* gimp
* mega
* simplenote

##### Stacer (from terminal)
```
sudo apt-get update -y
sudo apt-get upgrade -y
```
Download latest version from sourceforge..
```
wget https://jaist.dl.sourceforge.net/project/stacer/v1.0.9/stacer_1.0.9_amd64.deb
```
Install downloaded..
```
sudo dpkg -i stacer_1.0.9_amd64.deb
```
Search Stacer in app center

Also see [https://www.howtoforge.com/tutorial/how-to-install-stacer-system-monitoring-on-ubuntu-1804-lts/](https://www.howtoforge.com/tutorial/how-to-install-stacer-system-monitoring-on-ubuntu-1804-lts/)

##### VLC media player (from terminal)
```
sudo apt-get update
sudo apt-get install vlc
```
##### Atom editor (from terminal)
```
sudo add-apt-repository ppa:webupd8team/atom
sudo apt update; sudo apt install atom
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

##### Tabula for scraping PDFs (from terminal)

Download tabula-jar.zip from the download site [https://tabula.technology/](https://tabula.technology/) and unzip it to the directory of your choice. Open a terminal window, and cd to inside the tabula directory you just unzipped. Then run:

```
java -Dfile.encoding=utf-8 -Xms256M -Xmx1024M -jar tabula.jar
```
Then manually navigate your browser to http://127.0.0.1:8080/ 
If the program fails to run, double-check that you have Java installed and then try again.

1. Upload a PDF file containing a data table. 
2. Browse to the page you want, then select the table by clicking and dragging to draw a box around the table.
3. Click "Preview & Export Extracted Data". Tabula will try to extract the data and display a preview. Inspect the data to make sure it looks correct. If data is missing, you can go back to adjust your selection.
4. Click the "Export" button.
5. Now you can work with your data as text file or a spreadsheet rather than a PDF! 

Source [https://github.com/tabulapdf/tabula](https://github.com/tabulapdf/tabula)
Source [https://alignedleft.com/resources/pdf-data-extraction-tools](https://alignedleft.com/resources/pdf-data-extraction-tools)

##### youtube-dl (from terminal)

0. Remove/purge old version of youtube-dl, if needed
```
sudo apt-get remove <application_name> ## removes only the package
sudo apt-get purge <package-name> ## removes package + its config files
sudo apt-get autoremove ## run this after a purge
```
1. Update and upgrade repos
```
sudo apt-get update -y
sudo apt-get upgrade -y
```
2. Install curl
```
sudo apt-get install curl -y
```

3. Install youtube-dl binary
```
sudo curl -L https://yt-dl.org/latest/youtube-dl -o /usr/bin/youtube-dl
```

4. Change permissions
```
sudo chmod 755 /usr/bin/youtube-dl
```

5. Add PPA
```
sudo add-apt-repository ppa:nilarimogard/webupd8
```

6. Update package repo
```
sudo apt-get update -y
sudo apt-get install youtube-dlg -y
``` 

To use youtube-dl:

* install all the available options
```
youtube-dl --h
```
* download a playlist as mp4 (format code = 18)
```
youtube-dl -f 18 https://www.youtube.com/watch?v=j_JgXJ-apXs
```
* if you want to check available formats 
```
youtube-dl -F https://www.youtube.com/watch?v=j_JgXJ-apXs
```
* download mp3 format
```
youtube-dl https://www.youtube.com/watch?v=j_JgXJ-apXs -x --audio-format mp3
```
* if the playlist is behind a proxy
```
youtube-dl --proxy http://proxy-ip:port https://www.youtube.com/watch?v=j_JgXJ-apXs
```
* download from a specified list of URLs
```
youtube-dl -a youtube-list.txt ## but first save URLs in youtube-list.txt, one per line
``` 

Source [https://askubuntu.com/questions/784240/how-can-i-download-a-youtube-playlist](https://askubuntu.com/questions/784240/how-can-i-download-a-youtube-playlist) 
Source [https://www.howtoforge.com/tutorial/install-and-use-youtube-dl-on-ubuntu-1604/](https://www.howtoforge.com/tutorial/install-and-use-youtube-dl-on-ubuntu-1604/)

##### texlive for knitr (from terminal)
```
sudo apt-get update
sudo apt-get install texlive-latex-extra
```
Source [https://linuxconfig.org/how-to-install-latex-on-ubuntu-18-04-bionic-beaver-linux](https://linuxconfig.org/how-to-install-latex-on-ubuntu-18-04-bionic-beaver-linux) 

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

Fix Firefox plugin installation (64-bit only)
```
sudo rm -f /usr/lib/mozilla/plugins/npwrapper.npica.so /usr/lib/firefox/plugins/npwrapper.npica.so
sudo rm -f /usr/lib/mozilla/plugins/npica.so
sudo ln -s /opt/Citrix/ICAClient/npica.so /usr/lib/mozilla/plugins/npica.so
sudo ln -s /opt/Citrix/ICAClient/npica.so /usr/lib/firefox-addons/plugins/npica.so
```

Configure Firefox
In Firefox, go to Tools -> Add-ons -> Plugins, and make sure the "Citrix Receiver for Linux" plugin is set to "Always Activate".

Source [https://askubuntu.com/questions/40723/how-do-i-install-citrix-receiver#44137](https://askubuntu.com/questions/40723/how-do-i-install-citrix-receiver#44137)

##### R and RStudio

Step 1. From terminal:
```
sudo apt install r-base-core
```

Step 2. Download RStudio from [https://www.rstudio.com/products/rstudio/download/#download](https://www.rstudio.com/products/rstudio/download/#download)
Go to Downloads > right-click rstudio-xenial-1.1.453-amd64.deb > Open with Software Install > Install
To launch, Search your computer > type "RStudio"

Source [https://www.youtube.com/watch?v=P8wx4HY9me0](https://www.youtube.com/watch?v=P8wx4HY9me0)

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




