# Tp-Link-TL_WIN_722N Version 2/3



This helps in installing the required drivers for Tp-Link WiFi adapter

### TP-Link [TL-WIN722N] V 2/3 adapter settings for latest kali release

Install the below commands in order!

`sudo apt update`
<br>
`sudo apt install bc`
<br>
`sudo rmmod r8188eu.ko`
<br>
`git clone https://github.com/aircrack-ng/rtl8188eus`
<br>
`cd rtl8188eus`
<br>
`sudo -i`
<br>
`echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"`
<br>
`exit`
<br>
`make`
<br>
`sudo make install`
<br>
`sudo modprobe 8188eu`
<br>

### To enable Monitor mode

`ifconfig wlan0 down`
<br>
`airmon-ng check kill`
<br>
`iwconfig wlan0 mode monitor`
<br>
`ifconfig wlan0 up`
<br>
`iwconfig`
<br>

Once every thing is done and executed perfectly ,check mode of the WiFi adapter if the monitor mode is enabled. 
