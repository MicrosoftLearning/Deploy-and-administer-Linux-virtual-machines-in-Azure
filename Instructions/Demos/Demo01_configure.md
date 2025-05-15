---
demo:
    title: 'Demo 01: Configure an Azure Linux virtual machine'
    module: 'Guided Project: Deploy and administer Linux virtual machines'
---

# Demo 01: Configure an Azure Linux virtual machine

## Job skills

+ Create a Linux virtual machine (portal).
+ Configure a Linux VM.
+ Connect to a Linux VM with SSH.  
+ Update Linux VM operating systems.
+ Install and run a workload dependency.

## Resource requirements

This resource can be created before or during the demonstration. 

+ Resource group. 

## Reference slides (optional)

+ Plan for virtual machines
+ Supported Linux distributions
+ Virtual machine sizing
+ Azure resource organization
+ Azure Administrator tools

## Reference steps

Detailed steps are provided in these links.

+ [Provision a Linux virtual machine by using the Azure portal](https://learn.microsoft.com/training/modules/provision-linux-virtual-machine-in-azure/2-provision-linux-virtual-machine-using-the-azure-portal)
+ [Quickstart: Create a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu)

## Discussion points

**Creating and configuring the virtual machine**

1. Use the portal to create a Linux VM. Discuss how, in later exercises, the CLI and Quickstart templates will be used to create VMs. 

1. Use the portal link to review the Linux **Images** selection.  Identify the latest Ubuntu distribution.

1. Use the portal link to review the **Size** selections.  Discuss how you could scale the CPU and memory settings.

1. Discuss the effects of resizing. Resizing will be done in a later lab. 

1. Discuss the different ways of connecting to a Linux virtual machine (SSH public key and Password).
   
1. Discuss the importance of **inbound port rules**. Specifically, port 22 for SSH and port 80 for Nginx. 

1. Use the **Disks** tab to show how  a data disk would be added. Adding a data disk will be done in a later exercise. 
 
1. Use the **Advanced** page to show where a cloud-init file could be provided.

1. Also, later exercises use templates and the CLI to install virtual machines. 

**Access the virtual machine and install Nginx**

1. Deploy the virtual machine. Discuss the validation phase and how to monitor notifications.

1. Open a CMD window and access the virtual machine with SSH. Discuss the format of the SSH command and the location of the key file. 

1. Install Nginx and ensure the home page displays. 
