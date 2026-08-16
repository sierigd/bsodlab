Host: HOST-02
OS: Devuan GNU/Linux
Virtualization: KVM/libvirt

Hardware:
- Intel Core i5-4570
- 24GB RAM
- 750 GB Storage

Networking:
- Intel I217-LM (Physical, onboard NIC)
- br0 (bridge libvirt device)
- libvirt configuration:
<XML>
 <interface type="bridge">
  <mac address="52:54:00:16:0b:60"/>
  <source bridge="br0"/>
  <model type="virtio"/>
  <address type="pci" domain="0x0000" bus="0x01" slot="0x00" function="0x0"/>
 </interface>
</XML>

VMs:
- Win10 
	-OS: Windows 10 Professional
	-vCPU: 1
	-RAM: 6 GB
	-Storage: 40 GB
- Win11
	-OS: Windows 11 Professional
	-vCPU: 2
	-RAM: 6 GB
	-Storage: 40 GB
- RSAT
	-OS: Windows 10 Professional
	-vCPU: 2
	-RAM: 6 GB
	-Storage: 40 GB


Storage:
- 256GB SSD (host installation / qcow2 location)
- 500GB HDD (backups)
- Timeshift used for system backups (libvirt folders included), qcow2 is backed up manually.


