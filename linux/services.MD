/etc/edm/autostart
- those services run under a suser and not root

# Journalctl
C | A
 -|-
journalctl -u <service_name> | Filter by name
journalctl -u <service_name> -f | Follow logs
journalctl -u <service_name> -f -b | Follow logs for last boot (solves timestamp sqew problem)
rm /var/log/journal/... | remove journal files