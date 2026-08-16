Networking

A libvirt bridge is configured to allow virtual machines to participate directly on the local network where appropriate. This approach allows for a more realistic way of accessing the local network, as opposed to using the host's physical NIC directly on the VMs.

Example configuration concept:

	Physical
	  NIC
	  |
	 br0
	  |
  +-------+-------+
  |	  |	  |
  VM	  VM	  VM	 
  
  

Following is the XML definition for the bridge device on KVM:

<interface type="bridge">
  <mac address="52:54:00:16:0b:60"/>
  <source bridge="br0"/>
  <model type="virtio"/>
  <address type="pci" domain="0x0000" bus="0x01" slot="0x00" function="0x0"/>
</interface>



Hosts are connected directly to a Linksys home router using ethernet (802.11 was used in a previous iteration of the lab, requiring extra configuration for the bridge connection: ethernet simplified the setup).
