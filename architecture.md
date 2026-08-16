Architecture

Environment consists of two physical Linux virtualization hosts connected through ethernet to the home network. Both hosts feature identical hardware, and run Devuan Linux and use KVM/libvirt for virtualization. Windows and Linux infrastructure used for enterprise simulation are provided through virtual machines. 

A simplified view of the architecture would be:


               		   Home Network
                              |
                    +---------+---------+
                    |                   |
              Virtualization       Virtualization
                Host 01              Host 02
              (Devuan/KVM)         (Devuan/KVM)
                    |                   |
                    |	      +---------+--------+
          	    |         |         	 |
	          DC01       Windows		RSAT
                    |	     Client VMs		Workstation
          	    |         |                  | 
          	    +---------+------------------+
                         |
                    Active Directory
                         |
          +--------------+--------------+
          |              |              |
        Users         Groups           GPOs
          |
     Windows Clients
          |
      RSAT / PowerShell
