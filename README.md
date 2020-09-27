# KaliPi4
Setting the Raspberry Pi to monitor mode using the internal network adapter. Requires Ubuntu OS/ Kali OS/ Parrot OS/ Raspbian OS

### Update the package lists for Upgrades and fetch new versions of packages 
```
  sudo apt-get update && sudo apt-get ugprade
```

### Install aircrack-ng tools if not installed
```
  sudo apt-get install -y aircrack-ng
```

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
