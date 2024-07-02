---
demo:
    title: 'Demo 04 - Backup virtual machines'
    module: 'Guided Project: Backup virtual machines'
---

# Demo 04: Backup Azure virtual machines

Use this demonstration to review this task:
+ Configure Azure Backup 

## Demonstration steps

Use this [Quickstart: Backup virtual machines in the portal](https://learn.microsoft.com/azure/backup/quick-backup-vm-portal). 

## Reference slides

There are no additional slides to support the demonstration. 

## Discussion points

1. Discuss the need for a recovery services vault. The vault must be in the same region as the data source. 

1. Review how virtual machine backup can be enabled in the portal (vault, virtual machine, backup center).

1. Use the **datasource type** drop-down to review the many resources the Backup Center can protect.

1. Point out the default backup policy and that a custom backup policy can be created.

1. Discuss how a single backup policy can be used across many different virtual machines.

1. Review the backup policy configuration settings (schedule and retention).

1. Review how to monitor backup jobs.

1. Review how you can restore virtual machines (not on the credential). 
