SYNC-01 - Cloud synchronization server


Virtual Machine

Host:HOST01
OS: Windows Server Core 2022
vCPU: 2
RAM: 4GB
Network: br0

SYNC-01 was deployed as a separate Windows Server 2022 Desktop Experience VM because Microsoft Entra Connect Sync requires a supported GUI-based Windows Server installation. The Domain Controller remains Windows Server Core to minimize attack surface and resource consumption.

Network Configuration

VM uses libvirt br0 bridge
VirtIO drivers were installed from virtio-win ISO.

Virtual NIC was configured with:
- Dynamic IP (DHCP)
- DNS pointing to DC01

Installed Roles and Features

- Entra Connect

Domain Join

SYNC-01 was joined to the domain in order for Entra Connect to be able to sync with local domain instead of installing Entra Connect on the DC, as recommended by Microsoft themselves.


Backup / Recovery

After validating functionality

- VM snapshot created
- SYNC-01 qcow2 backed up to a separate storage
- libvirt configuration included in host backups
- Timeshift backup of host configuration retained
