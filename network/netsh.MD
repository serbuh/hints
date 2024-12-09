cmd | action
-|-
netsh WLAN show profiles | Profiles list
netsh WLAN show drivers | Drivers
netsh WLAN show interfaces | Interfaces
netsh WLAN show profile name="network_SSID_name" key=clear | View profile (with key)
netsh WLAN delete profile name="network_SSID_name" | Delete profile
netsh WLAN export profile key=clear folder="C:" | Export all to file
netsh WLAN export profile name="network_SSID_name" key=clear folder="C:" | Export specific to file
netsh WLAN add profile filename="C:\WiFi.xml" | Import from file
netsh WLAN connect | Connect
netsh wlan show wlanreport | Report
