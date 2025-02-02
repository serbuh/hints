Fix error mounting:
```
sudo ntfsfix /dev/sda1
```

C | A
-| -
blkid | Get UUID
lsblk -o NAME,UUID,MOUNTPOINT | Get UUID

## Mount with fstab
`sudo cp /etc/fstab /etc/fstab.bkup`
`vim /etc/fstab`
Add:
`UUID=1234-5678  /mnt/mydisk  ext4  defaults  0  2`

Unmount: `sudo umount /mnt/ssd`
Mount: `sudo mount -a`