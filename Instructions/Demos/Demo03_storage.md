---
demo:
    title: 'Demo 03: Access storage for an Azure Linux virtual machine'
    module: 'Guided Project: Deploy and administer Linux virtual machines'
---

# Demo 03: Access storage for an Azure Linux virtual machine

## Job skills

+ Create a virtual machine (CLI).
+ Add virtual machine data disks and configure partitions. 
+ Mount an SMB Azure file share on a Linux VM.
+ Assign a managed identity on a Linux VM. 
+ Assign Azure roles. 
+ Transfer data to and from a Linux VM by using AzCopy. 

## Resource requirements

These resources can be created before or during the demonstration. 
+ Resource group
+ Linux virtual machine.
+ Storage account with file share and blob container.
+ Uploaded files to use for testing.
+ Managed identity. 

## Reference steps

Detailed steps are provided in these links.

+ [Quickstart: Create a Linux virtual machine with the Azure CLI on Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli)
+ [Attach a data disk to a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/attach-disk-portal)
+ [Create an SMB file share](https://learn.microsoft.com/azure/storage/files/storage-how-to-create-file-share?tabs=azure-portal)
+ [Get started with AzCopy](https://learn.microsoft.com/azure/storage/common/storage-use-azcopy-v10)


## Reference slides

Use these slides for additional context. 
+ Storage accounts
+ Blob containers and files
+ Files versus blobs
+ Managed identities
+ Role-based access control

## Discussion points

**Create a virtual machine using CLI** - Reference #1

>You can use an existing vm, rather than create another one.

1. Access the Cloud Shell.

1. Create the virtual machine with CLI. Point out this is the third way students have been shown to create vms.
   
**Add a data disk to a Linux virtual machine** - Reference #2

1. Review how to use the portal to add a data disk to a virtual machine. Students will use CLI in the exercise.

1. Connect to the virtual machine and use `lsblk` to list the disks. Note the disk size and that the disk is not mounted.

1. Prepare the disk with `parted` and `partprobe`. Use the code in the reference link.

1. Mount the disk and use `df` to list the mount point. 

**Access an SMB file share from the virtual machine** - Reference #3 and student lab instructions

1. Locate the storage account and discuss file shares.

1. Assign a managed identity to the virtual machine. The identity should have access to the storage account.

1. Copy the portal script to access the file share from a Linux virtual machine.

1. Connect to the virtual machine and create a file with the script. You can use the vi editor.

1. Run the script and mount the file share. 

**Use AzCopy to copy a blob file to the data drive** - Reference #4 and the student lab instructions.

1. Add the Blob Data Storage Contributor role to the virtual machine. Review other blob roles. 

1. Connect to the virtual machine and install AzCopy. Review other tools that can be used for transfering files. 

1. Use AzCopy to transfer a file from blob storage to the data drive. You can also transfer a file back to blob storage.  
