Disaster Recovery

The lab has already been used to test recovery from a physical SSD failure.
The incident demonstrated the importance of separating:

- Host operating systems
- VM storage
- Backups
- Configuration documentation

Following the incident, backup architecture was improved. Recovery procedure for host is now intended to be:

- Reinstall Devuan
- Restore host configuration from Timeshift host backup
- Continue with recovery procedure for other components of the lab (VMs, Domain controller, etc.)

