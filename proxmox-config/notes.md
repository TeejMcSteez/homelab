## Proxmox Config Notes

### Install

1. Install [Latest](https://www.proxmox.com/en/downloads) Proxmox ISO to USB
2. Once booted into bootloader, ctrl+x to edit boot config, add nomodeset to config
    - **nomodeset** stops probing of all equipment used for older devices were probing equipment takes forever.
3. Load into proxmox server and create account.
4. Load USB backup and mount onto the Proxmox machine
5. Restore backups from USB drive.

### Home Assistant (Quirky)

To install Home Assistant to recover from backup requires you to make an empty VM on Proxmox and then mount the [.qcow2](https://www.home-assistant.io/installation/alternative) image to a drive and then point the VM at that drive. Starts a headless instance of Home Assistant running soely through Proxmox (no host Ubuntu/Docker server etc.)

1. Install Latest [.qcow2](https://www.home-assistant.io/installation/alternative) image from [Home Assistant](https://www.home-assistant.io/)
2. copy/mount [.qcow2](https://www.home-assistant.io/installation/alternative) image to a drive on host machine through smb, ssh, etc.
3. Create a VM with no storage device
4. After creating add a storage device to the VM and point it to the drive where you mounted the [.qcow2](https://www.home-assistant.io/installation/alternative) image