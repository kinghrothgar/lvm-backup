# LVM-BACKUP

## Requirements:
1. LVM Logical Volume (LG) in Volume Group (VG) that has free space
2. Install programs: `tar`, `pigz`

## How To Use:
1. Place all files in the same paths found in this repo.
2. Edit /opt/bin/snapshot_lvm changing `SNAP_SIZE` to something slightly smaller than the available space in your VG
3. Edit /opt/bin/backup_lvm to suite your needs, specifically setting the `DEST` to the backup folder
4. If you have an logical volume called `rootfs`, run `systemctl start lvm-backup@rootfs`

## TODO:
* Add an exclude list
* Show how to utilize a remove backup location with ssh
