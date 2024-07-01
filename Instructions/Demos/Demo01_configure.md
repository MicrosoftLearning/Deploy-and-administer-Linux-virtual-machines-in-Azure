---
demo:
    title: 'Demo 01 - Configure virtual machines'
    module: 'Guided Project: Configure virtual machines'
---

# Demo: Configure virtual machines

## Demonstration steps

Use this Learn page [Provision a Linux virtual machine by using the Azure portal](https://learn.microsoft.com/training/modules/provision-linux-virtual-machine-in-azure/2-provision-linux-virtual-machine-using-the-azure-portal) for your demonstration. 

Alternatively, you can use the [Quickstart: Create a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu)

## Reference slides

    


## Discussion points

**Creating and configuring the virtual machine**
1. Use the portal link to review the Linux **Images** selection.  Identify the "lastest" Ubuntu distribution. 
2. Use the portal link to review the **Size** selections.  Discuss how you could scale the CPU and memory settings. 
3. Discuss the different ways of connecting to a Linux virtual machine (SSH public key and Password).
4. Discuss the importance of **inbound port rules**. Specifically, port 22 for SSH and port 80 for Nginx. 
5. Use the **Advanced** page to show where a cloud-init file could be provided.
6. Emphasize more details (storage, monitoring) will be added in later exercises.
7. Also, later exercises use templates and the CLI to install virtual machines. 

**Access the virtual machine and install Nginx**
1. Deploy the virtual machine.
2. Access the virtual machine with SSH. Discuss the format of the SSH command and the location of the key file. 
3. Install Nginx and ensure the home page displays. 
