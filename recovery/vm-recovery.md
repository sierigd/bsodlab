Client VMs recovery

The lab has already been used to test recovery from a physical SSD failure.
Following the incident, backup architecture was improved. 

Now the recovery procedure for the client VMs is intended to be:

- Restore libvirt configuration from Timeshift backup whenever possible. Otherwise create a new VM for the client with the configuration outlined in the documentation (resource assignment, network bridge -br0-).
- Copy qcow2 VM image corresponding to VM from backup storage back to the current VM directory
- Confirm connectivity with local network and Domain Controller (if up). Join the VM(s) to the domain once done
