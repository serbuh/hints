C|A
-|-
sudo ntpdate \<ip\> | Update date from ntp server
sudo date MMDDhhmmYYYY | Update date (short format)
sudo date --set="2025-02-02 14:30:00" | Update date 

## Persistant ntp timesync
Modify:
```
sudo nano /etc/systemd/timesyncd.conf
```
Add:
```
NTP=<ntp_server>
```
Restart timesync service
```
sudo systemctl restart systemd-timesyncd
```