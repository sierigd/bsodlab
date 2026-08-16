Domain controller recovery

The lab has already been used to test recovery from a physical SSD failure.
Following the incident, backup architecture was improved. 

Now the recovery procedure for the domain controller is intended to be:

- Restore libvirt configuration from Timeshift backup if possible. Otherwise create a new VM for the Domain Controller with the configuration outlined in the documentation (resource assignment, network bridge -br0-).
- Copy qcow2 VM image corresponding to DC-01 from backup storage back to the current VM directory
- Confirm connectivity with local network and client VMs (once up)
