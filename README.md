## project auto mount file system when system boot
##to check disk mount point 
lsblk
```
sudo blkid
```
/dev/sda5: UUID="1198c353-ecab-481b-82fe-9dfd29267a47" TYPE="ext4" PARTUUID="3fca5c1b-05"
/dev/sr0: UUID="2023-10-12-17-41-58-38" LABEL="VBox_GAs_7.0.12" TYPE="iso9660"
/dev/sda1: UUID="A90F-3080" TYPE="vfat" PARTUUID="3fca5c1b-01"
```
sudo mkdir /mnt/sda5
```
## sudo nano /etc/fstab
### UUID=<uuid-of-your-drive>  <mount-point>  <file-system-type>  <mount-option>  <dump>  <pass>
UUID=1198c353-ecab-481b-82fe-9dfd29267a47       /mnt/sda5       ext4    defaults        0       2
```
sudo mount -a
## to check mount done or not
mount | grep ext4 0r cd /mnt/sda5/
#problem with this mount
```
 the system must dedicate resources to keep the mounted file system in place. This is not a problem with one or two mounts, but when the system is maintaining mounts to many 
 systems at one time, overall system performance can be affected



