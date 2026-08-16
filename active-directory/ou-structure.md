The Active Directory environment is designed to resemble a small enterprise rather than a flat collection of test objects.
The planned OU structure is:
LAB
|
+-- Users
|
+-- Groups
|
+-- Workstations
|   |
|   +-- Test
|
+-- Servers
|
+-- Administrative
|
+-- Disabled


The exact structure may evolve as additional services are introduced.

OU structure creation is also automated through PowerShell scripting (see /powershell/ for more information)
