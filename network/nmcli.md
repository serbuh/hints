cmd | action
-|-
nmcli dev wifi list | List wifi
nmcli connection show | List connections
nmcli dev wifi connect "SSID" --ask | Connect to wifi
nmcli dev wifi connect "SSID" --ask ifname wlan0 | Connect to wifi
nmcli dev wifi connect "SSID" password "pass" | Connect to wifi
nmcli con edit Buh | edit connection