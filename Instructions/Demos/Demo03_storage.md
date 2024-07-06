---
demo:
    title: 'Demo 03: Access storage for virtual machines'
    module: 'Guided Project: Access storage for virtual machines'
---

# Demo 03: Storage for virtual machines

## Credential tasks

+ Add data disks and configure partitions. 
+ Mount an SMB Azure file share on a Linux VM.
+ Assign a managed identity on a Linux VM. 
+ Assign Azure roles. 
+ Transfer data to and from a Linux VM by using AzCopy. 

## Resource requirements

These resources can be created before or during the demonstration. 
+ Linux virtual machine.
+ Storage account with file share and blob container.
+ Uploaded files to use for testing.
+ Managed identity. 

## Reference steps

Detailed steps are provided in these links.

+ [Quickstart: Create a Linux virtual machine with the Azure CLI on Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli)
+ [Attach a data disk to a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/attach-disk-portal)
+ [Create a virtual machine with the CLI](https://learn.microsoft.com/azure/virtual-machines/linux/quick-create-cli)
+ [Create an SMB file share](https://learn.microsoft.com/azure/storage/files/storage-how-to-create-file-share?tabs=azure-portal)


## Reference slides

Use these slides for additional context. 
+ Storage accounts
+ Blob containers and files
+ Files versus blobs
+ Role-based access control
+ 

## Discussion points

**Create a virtual machine using CLI**

>You can use an existing vm, rather than create another one.

1. Access the Cloud Shell.

1. Create the virtual machine with CLI. Point out this is the third way students have seen to create vms.
   
**Add a data disk to a Linux virtual machine** - Reference #1

1. Review how to use the portal to add a data disk to a virtual machine. Students will use CLI in the exercise.

1. Connect to the virtual machine and use `lsblk` to list the disks. Note the disk size and that the disk is not mounted.

1. Prepare the disk with `parted` and `partprobe`. Use the code in the reference link.

1. Mount the disk and use `df` to list the mount point. 

**Access an SMB file share from the virtual machine**

>These steps are documented in the student lab instructions.

1. Locate the storage account and review file shares.

1. Assign a managed identity to the virtual machine. The identity should have access to the storage account.

1. Copy the portal script to access the file share from a Linux virtual machine.

1. Connect to the virtual machine and create a file with the script. You can use the vi editor.

1. Run the script

** 
