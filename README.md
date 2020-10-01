# PirCrack4
Setting the Raspberry Pi to monitor mode using the internal network adapter. Requires Kali OS with the nexmon patch available here https://www.offensive-security.com/kali-linux-arm-images/ and download the version **Kali Linux RaspberryPi 2 (v1.2), 3 and 4 (64-Bit)**. 

## IMPORTANT 
I am not responsible to any damage that is caused by misusing the commands or any damage to your device (This will probably never happen).
Preferable to use an external network adapter which supports MONITOR MODE. This can help you to hear nearby devices in the 5GHz bandwith too.
Find the name of the wireless adapter by using the iwconfig command.
Use the name of the (wirelessAdapter) in place of wlan0mon below

### Update the package lists for Upgrades and fetch new versions of packages using
```
  sudo apt-get update && sudo apt-get ugprade
```

### Install aircrack-ng tools if not installed using
```
  sudo apt-get install -y aircrack-ng
```

## To run the script: Clone the repository and use
```
  chmod +x script.sh
  ./script.sh
```

## Alternatively run the commands:

### To check for connected wireless extensions
```
  iwconfig
```

### If you plan to use the internal wireless adapter then you should find an option called wlan0.
```
  airmon-ng start wlan0
```

#### Don't worry about the error 'command failed: unknown error 524'. wlan0mon should appear at the bottom when you type iwconfig

### Kill processes using
```
  airmon-ng check kill
```

### To hear nearby devices (Final Step) 
```
  airodump-ng wlan0mon
```
