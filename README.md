# LVM-BACKUP

## Requirements:
1. LVM Logical Volume (LV) in Volume Group (VG) that has free space
2. Another partition other than the LV you are backing up with enough space for the backup
3. Install programs: `tar`, `pigz`

## How To Use:
1. Place all files in the same paths found in this repo.
2. Edit /opt/bin/snapshot_lvm changing `SNAP_SIZE` to something slightly smaller than the available space in your VG
3. Edit /opt/bin/backup_lvm to suite your needs, specifically setting the `DEST` to the backup folder
**NOTE:** DO NOT SET `DEST` TO A PATH IN ON THE LV YOU ARE BACKING UP
4. If you have an logical volume called `rootfs`, run `systemctl start lvm-backup@rootfs`

## TODO:
* Add an exclude list
* Show how to utilize a remove backup location with ssh
