# Tp-Link-TL_WIN_722N Version 2/3



# TP-Link [TL-WIN722N] V 2/3

This helps in installing the required drivers for Tp-Link WiFi adapter

### TP-Link [TL-WIN722N] V 2/3 adapter settings for latest kali release

Install the below commands in order!
---
`sudo apt update`
<br>
<br>

`sudo apt install bc`
<br>
<br>

`sudo rmmod r8188eu.ko`
<br>
<br>

`git clone https://github.com/aircrack-ng/rtl8188eus`
<br>
<br>

`cd rtl8188eus`
<br>
<br>

`sudo -i`
<br>
<br>

`echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"`
<br>
<br>

`exit`
<br>
<br>

`make`
<br>
<br>

`sudo make install`
<br>
<br>

`sudo modprobe 8188eu`
<br>
<br>

### To enable Monitor mode

<br>

`ifconfig wlan0 down`
<br>
<br>
`airmon-ng check kill`
<br>
<br>
`iwconfig wlan0 mode monitor`
<br>
<br>
`ifconfig wlan0 up`
<br>
<br>
`iwconfig`
<br>
<br>

### Once every thing is done and executed perfectly ,check mode of the WiFi adapter if the monitor mode is enabled. 
