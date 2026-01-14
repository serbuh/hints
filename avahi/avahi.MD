C|A
-|-
/etc/avahi/avahi-daemon.conf | Avahi config
sudo tcpdump -ni wlan0 udp port 5353 | listen for packets from avahi
avahi-browse -a | show discovered services
avahi-browse -a -r | show resolved services

+ line = service discovered (announcement seen), but details not resolved yet.
= line = service resolved (hostname, address, port, TXT obtained).

### Resolve concrete service:
`avahi-browse -rtp _zvuv._udp`
`-r` = resolve discovered services (hostname, IP, port, TXT).
`-t` = terminate after the first full browse/resolution pass.
`-p` = “parsable” output (semicolon‑separated lines).
