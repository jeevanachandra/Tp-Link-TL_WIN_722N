# Tp-Link-TL_WIN_722N Version 2/3


This helps in installing the required drivers for Tp-Link WiFi adapter

### TP-Link [TL-WIN722N] V 2/3 adapter settings for latest kali release

Install the below commands in order!

`sudo apt update`
`sudo apt install bc`
`sudo rmmod r8188eu.ko`
`git clone https://github.com/aircrack-ng/rtl8188eus`
`cd rtl8188eus`
`sudo -i`
`echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"`
`exit`
`make`
`sudo make install`
`sudo modprobe 8188eu`

### To enable Monitor mode

`ifconfig wlan0 down`
`airmon-ng check kill`
`iwconfig wlan0 mode monitor`
`ifconfig wlan0 up`
`iwconfig`

Once every thing is done and executed perfectly ,check mode of the WiFi adapter if the monitor mode is enabled. 
