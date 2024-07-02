---
demo:
    title: 'Demo 03: Access storage for virtual machines'
    module: 'Guided Project: Access storage for virtual machines'
---

# Demo 03: Storage for virtual machines

Use this demonstration to review these credential tasks:
+ Add data disks and configure partitions  
+ Mount an SMB Azure file share on a Linux VM 
+ Assign a managed identity on a Linux VM 
+ Assign Azure roles 
+ Transfer data to and from a Linux VM by using AzCopy 

## Reference slides

Use these slides for additional context. 
    


## Discussion points

**Add a data disk to a Linux virtual machine**

Reference: [Use the portal to attach a data disk to a Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/attach-disk-portal)

>These steps require a Linux virtual machine. 

1. Review how to use the portal to add a data disk to a virtual machine. Students will use CLI in the exercise.

1. Connect to the virtual machine and use `lsblk` to list the disks. Note the disk size and that the disk is not mounted.

1. Prepare the disk with `parted` and `partprobe`. Use the code in the demonstration.

1. Mount the disk and verify it is available.

**Access an SMB file share from the virtual machine**

1. 
