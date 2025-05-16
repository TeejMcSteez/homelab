## Notes

Backups are stored on USB plugged into host in case of brown out or death, the nightly (21:00) backup can be used to restore the system.

Currently TrueNAS is my biggest backup as it also backups the data inside the VM. So depending on how much data one has in their NAS they may want it seperate entirely or to not backup to USB and use different methods of data integrity.

This is fine for me now as I mainly use it for shares and storing non-important installers, ISO's, Code, etc.

## Config

System uses Snapshot mode backups with ZSTD (fast and good) compression.

## Backup Inventory

**Backed Up**

1. Ubuntu (VM)
2. TrueNAS (VM)
3. HAS (VM)

**Retention**: Keeps back ups from past 3 days, USB is 64GB otherwise would overload with VM information. Can be changed for amount of information stored in backup or for more redundancy right now 3 days is the middle road for my system.