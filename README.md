# KaliPi4
Using Kali on Raspberry Pi 4 with internal network adapter for basic aircrack tools and attacks

### Update the package lists for Upgrades and fetch new versions of packages 
'''
  sudo apt-get update && sudo apt-get ugprade
'''

### Install aircrack-ng tools if not installed
'''
  sudo apt-get install -y aircrack-ng
'''

### To check for connected wireless extensions
'''
  iwconfig
'''

### If you plan to use the internal wireless adapter then you should find an option called wlan0.
'''
  airmon-ng start wlan0
'''

### Don't worry about the error 'command failed: unknown error 524'. wlan0mon should appear at the bottom when you type iwconfig

### Kill processes using
'''
  airmon-ng check kill
'''

### Final Step to hear nearby devices
'''
  airodump-ng wlan0mon
'''
