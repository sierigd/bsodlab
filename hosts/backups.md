Backup strategy

Lab is designed around the assumption that individual systems can fail



Host Backups

Host OS is backed up using Timeshift before major changes or updates
Backups are synchronized to separate storage using scheduled (cron) rsync jobs.



VM Backups

Important VM disk images (qcow2) are backed up separately
Critical systems currently prioritized for backup include:

-DC01
-RSAT client

Other Windows client systems are considered reproducible and can be rebuilt from installation media (base snapshots for client systems are included as part of the backups)



Configuration backups

Important configuration data is stored separately from the running systems, including (but not limited to):

- BIOS configuration
- Host configuration
- Network configuration
- Lab documentation
- Powershell scripts
- GPO backups
- VM configuration information
