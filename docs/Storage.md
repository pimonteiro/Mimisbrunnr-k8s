# Homelab Storage Situation

For more context on the hardware, see [[Architecture]].

- **Bulkstorage:** 2 disks of 4TB each, in mirror mode, in TrueNAS Scale VM (StorageClasses: `truenas-nfs`, `truenas-iscsi`)
- **SelfCloud:** 2 disks of 512GB each, in mirror mode, in TrueNAS Scale VM (StorageClasses: `truenas-selfcloud-nfs`, `truenas-selfcloud-iscsi`)

## Offsite Backup (Disaster Recovery)
- **Target:** Hetzner Storage Box (`uXXXXXX.your-storagebox.de`, SFTP Port `23`)
- **Encryption:** Client-side AES-256 (TrueNAS Cloud Sync with Rclone Crypt overlay)
- **Schedule:** Nightly PUSH sync
- **Obsidian Documentation:** [[Hetzner-Storage-Box]] / `Obsidian/4. Homelab/Infrastructure/Storage/Hetzner-Storage-Box.md`