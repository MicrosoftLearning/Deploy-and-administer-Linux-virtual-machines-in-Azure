---
demo:
    title: 'Demo 01: Configure virtual machines'
    module: 'Guided Project: Configure virtual machines'
---

# Demo 01: Configure virtual machines

Use this demonstration to review these credential tasks:
+ Create a Linux virtual machine (VM) 
+ Configure a Linux VM 
+ Connect to a Linux VM with SSH   
+ Update Linux VM operating systems
+ Install and run a workload dependency


## Reference slides

Use these slides for additional context.
    


## Demonstration and discussion

+ [Provision a Linux virtual machine by using the Azure portal](https://learn.microsoft.com/training/modules/provision-linux-virtual-machine-in-azure/2-provision-linux-virtual-machine-using-the-azure-portal)

+ [Quickstart: Create a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu)
  
**Creating and configuring the virtual machine**

1. Use the portal link to review the Linux **Images** selection.  Identify the latest Ubuntu distribution.

1. Use the portal link to review the **Size** selections.  Discuss how you could scale the CPU and memory settings.

1. Discuss the different ways of connecting to a Linux virtual machine (SSH public key and Password).
   
1. Discuss the importance of **inbound port rules**. Specifically, port 22 for SSH and port 80 for Nginx.
 
1. Use the **Advanced** page to show where a cloud-init file could be provided.

1. Emphasize more details (storage, monitoring) will be added in later exercises.

1. Also, later exercises use templates and the CLI to install virtual machines. 

**Access the virtual machine and install Nginx**

1. Deploy the virtual machine.

1. Access the virtual machine with SSH. Discuss the format of the SSH command and the location of the key file. 

1. Install Nginx and ensure the home page displays. 
