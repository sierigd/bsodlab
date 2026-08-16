Host: HOST-01
OS: Devuan GNU/Linux
Virtualization: KVM/libvirt

Hardware:
- Intel Core i5-4570
- 32GB RAM
- 1.5 TB Storage

Networking:
- Intel I217-LM (Physical, onboard NIC)
- br0 (bridge libvirt device)


VMs:
- DC01 (AD Domain Controller):
	-OS: Windows Server Core 2022
	-vCPU: 1
	-RAM: 4 GB
	-Storage: 20 GB


Storage:
- 1TB SSD (host installation / qcow2 location)
- 500GB HDD (backups)
- Timeshift used for system backups (libvirt folders included), qcow2 is backed up manually.



