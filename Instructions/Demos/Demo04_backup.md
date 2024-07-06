---
demo:
    title: 'Demo 04: Backup virtual machines'
    module: 'Guided Project: Backup virtual machines'
---

# Demo 04: Backup Azure virtual machines

## Credential task

+ Configure Azure Backup 

## Resource requirements

+ Linux virtual machine

## Reference steps

Detailed steps are provided in this link.

+ [Quickstart: Backup virtual machines in the portal](https://learn.microsoft.com/azure/backup/quick-backup-vm-portal)
+ [Quickstart: Create and deploy ARM templates by using the Azure portal](https://learn.microsoft.com/azure/azure-resource-manager/templates/quickstart-create-templates-use-the-portal)

## Reference slides

Use these slides for additional context.  

+ What is Azure Backup?
+ Options to protect virtual machines

## Discussion points

1. Review importing a template is the fourth way they have created a vm in class.
   
1. Discuss the need for a recovery services vault. The vault must be in the same region as the data source. 

1. Review how virtual machine backup can be accessed and enabled in the portal. 

1. Discuss the difference between the Standard and Enhanced backup policies. 

1. Use the **datasource type** drop-down to review the resources the Backup Center can protect.

1. Point out the default backup policy and that a custom backup policy can be created.

1. Discuss how a single backup policy can be used across many different virtual machines.

1. Review the backup policy configuration settings (schedule and retention).

1. Review how to monitor backup jobs.

1. Review how you can restore virtual machines (not on the credential). 
