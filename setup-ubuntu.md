# Things to do after installing Ubuntu 16.04 LTS:

## 1. Open the terminal (Ctrl+Alt+T) and update + upgrade the system repos:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
## 2. Install essential tools
```
sudo apt-get install git
sudo apt-get install gksu
```
## 3. System Settings (left menu bar)
\> Appearance > Look (reduce launcher icon size to 40) > Behaviour (show menus in title bar, select always displayed)
\> Brightness & lock > (never turn off, lock OFF)
\> Security & Privacy > Files & Applications (Record usage OFF, clear usage data, untick all)
\> User Accounts (tick show my login in the menu bar)

## 4. Firefox preferences:
Open Firefox > Preferences
\> General (Home page [https://duckduckgo.com/](https://duckduckgo.com/))
\> Search (Set default search engine to [https://duckduckgo.com/](https://duckduckgo.com/))
\> Privacy & Security > History (set to Never Remember, clear all history, untick address bar suggestions, Tracking Protection: Always, Untick sending technical data to Firefox)

<hr>

# Install printer/scanner driver for SAMSUNG M2070W on Ubuntu 16.04 LTS:

## 1. Download the driver from [http://www.samsungdrivers.net/samsung-m2070-driver/](http://www.samsungdrivers.net/samsung-m2070-driver/)
Bottom of the page you'll see "Samsung M2070 Linux Printer/Scanner Driver Download (15.87 MB)"

## 2. Go to your Downloads directory and decompress the downloaded archive:
Right-click > Extract Here
(or in the terminal run: `tar -xvzf ULD_v1.00.29.tar.gz`)

## 3. Open the terminal (Ctrl+Alt+T) and navigate the uld directory:
cd Downloads/uld

## 4. Run the install-printer.sh file:
sudo sh ./install-printer.sh
(follow install instructions, y to confirm, Enter repeatedly to skip through the EULA)

## 5. Run the install-scanner.sh file:
```sudo sh ./install-scanner.sh```
(follow install instructions, Enter or y to confirm)

## 6. Connect the printer to your PC and turn it on

## 7. Open System Settings > Printers > Add > (select Samsung M2070) > Forward > Apply

<hr>

# Install VLC media player:
In the terminal (Ctrl+Alt+T) run:
```
sudo apt-get update
sudo apt-get install vlc
```


