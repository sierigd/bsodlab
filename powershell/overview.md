Powershell

Powershell is being incorporated as the primary automation and administration interface.
Main goal is not to simply memorize cmdlets, but to develop repeatable administrative workflows.
Current areas of study include:

- Objects and properties
- The pipeline
- Filtering and sorting
- Loops
- Functions
- Error handling
- Modules
- Active Directory administration
- Remoting
- Automation

Various automation projects are included as part of the lab

- OU Creation from CSV 

CSV file defines the desired OU structure.
what the script does:

1- Imports CSV
2- Validates requested paths
3- Checks whether each OU already exists
4- Creates missing OUs
5- Reports existing objects
6- Handles errors without stopping the entire operation

Script itself should be idempotent (running it repeatedly does not create duplicate objects)

- User provisioning from CSV

Users and their intended group memberships are defined through a CSV file.
Automation handles:

1- User creation
2- Display names
3- UPNs
4- Descriptions
5- OU placement
6- Security group membership
7- Account status

Example concept:

User -> Department -> OU
	|
	+--> Security Groups
	
Project goal is to demonstrate practical account-provisioning automation

- GPO Backup

Group Policy Objects are backed up using Powershell. Useful for disaster recovery, configuration history, change tracking and baseline reference (used in following automation project).

- GPO Baseline Comparison

Compares current GPO configuration against a known-good baseline, providing a quick and automated way to detect configuration drift. 
Implementation:

Baseline GPO backup -> Current GPO Backup -> Configuration Comparison -> Difference Report

- Entra Sync Preflight





