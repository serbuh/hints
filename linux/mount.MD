C | A
-| -
blkid | Get UUID
lsblk -o NAME,UUID,MOUNTPOINT | Get UUID
sudo mount -a | remount fstab
sudo umount /mnt/ssd | Unmount

## Mount with fstab
```
sudo cp /etc/fstab /etc/fstab.bkup
vim /etc/fstab
```
Add:
```
UUID=1234-5678  /mnt/mydisk  ext4  defaults  0  2
```
Mount
```
sudo mount -a
```

## Fix error mounting:
```
sudo ntfsfix /dev/sda1
```