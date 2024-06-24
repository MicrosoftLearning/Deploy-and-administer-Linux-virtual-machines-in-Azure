---
lab:
    title: 'Backup virtual machines'
    module: 'Backup virtual machines'
---
# Lab 04 - Backup a virtual machine

## Lab requirements    

This lab requires an Azure virtual machine. If you don't have a virtual machine, there are optional instructions to create one. 

This lab requires an Azure subscription. Your subscription type may affect the availability of features in this lab. You may change the regions, but the steps were tested using the **(US) East** region.

## Estimated timing: 30 minutes

## Lab scenario

Your organization is evaluating how to backup Azure virtual machines. Backup will protect the virtual machines from accidental or malicious data loss. You plan to explore using the Azure Backup Center.

## Interactive lab simulation

There is an interactive lab simulation that you might find useful for this topic. The simulation lets you to click through a similar scenario at your own pace. There are differences between the interactive simulation and this lab, but many of the core concepts are the same. An Azure subscription is not required.

+ **[Backup virtual machines and on-premises files.](https://mslabs.cloudguides.com/guides/AZ-104%20Exam%20Guide%20-%20Microsoft%20Azure%20Administrator%20Exercise%2016)**. Create a recovery services vault and implement an Azure virtual machine backup. Implement on-premises file and folder backup using the Microsoft Azure Recovery Services agent. On-premises backups are outside the scope of this lab but it might be helpful to view those steps. 

## Job skills

+ Task 1: Create and configure a Recovery Services vault.
+ Task 2: Configure Azure virtual machine-level backup.
+ Task 3: Configure a SMB File share backup. 
+ Task 4: Monitor Azure Backup.

## Estimated timing: 20 minutes

## Architecture diagram

!IMAGE[Architecture diagram for Lab 04.](instructions266099/lab04backup.png)

## Create a virtual machine (optional)

In this task, you will deploy a template to create a Linux virtual machine. 

1. In the Azure portal, search for and select `Deploy a custom template.`

1. Notice your choices and select **Create a Linux virtual machine.**

1. Take the defaults, except for these required settings. 

    | Settings | Value |
    | --- | --- |
    | Subscription | the name of your Azure subscription |
    | Resource group | `rg1`  |
    | Authentication type | **SSA Public Key** | 
    | Key pair name | `key_simpleLinuxvm` |
    | Admin user name | `adminuser` |

1. Click **Review + Create**, ensure that the validation passes and then click **Create**.

1. On the **Generate new key pairs** page select **Download + create**.

1. You can continue to the next task while the virtual machine deploys. 


## Task 1: Create and configure a Recovery Services vault

In this task, you will create a Recovery Services vault. 

>A [Recovery Services vault](https://learn.microsoft.com/azure/backup/backup-azure-recovery-services-vault-overview)  is a storage entity in Azure that houses data. The data is typically copies of data, or configuration information for virtual machines (VMs), workloads, servers, or workstations. 

1. In the Azure portal, search for and select `Recovery Services vaults`.

1. On the **Recovery Services vaults** blade, click **+ Create**.

1. On the **Create Recovery Services vault** blade, specify the following settings:

    | Settings | Value |
    | --- | --- |
    | Subscription | the name of your Azure subscription |
    | Resource group | `rg1`  |
    | Vault Name | `rsv1` |
    | Region | **(US) East** |

    >Make sure you use the same region as the virtual machines.

1. Click **Review + Create**, ensure that the validation passes and then click **Create**.

    >Wait for the deployment to complete. The deployment should take a couple of minutes. 

1. When the deployment is completed, click **Go to Resource**.

1. In the **Protected items** section select **Backup items**. Notice the vault does not yet contain any backups. 

    >**Check your learning**
    + Can you create and configure a Recovery Service vault for backups?  


## Task 2: Configure Azure virtual machine-level backup

In this task, you will implement Azure virtual-machine level backup. As part of a VM backup, you will define a backup and retention policy.

>When you [enable a virtual machine backup](https://learn.microsoft.com/azure/backup/quick-backup-vm-portal#enable-backup-on-a-vm) you can configure a backup schedule and retention range. 

1. Continue working on the Recovery Services vault, click **Overview**, then click **+ Backup**.

1. On the **Backup Goal** blade, specify the following settings:

    | Settings | Value |
    | --- | --- |
    | Where is your workload running? | **Azure** (notice your other options) |
    | What do you want to backup? | **Virtual machine** (notice your other options |

1. Select **Backup**.

1. Notice there a two **Policy sub types**: **Enhanced** and **Standard**. Review the choices and select **Enhanced**. 

1. In **Backup policy**, select **Create a new policy**.

1. Define a new backup policy with the following settings (leave others with their default values):

    | Setting | Value |
    | ---- | ---- |
    | Policy name | `vmbackup` |
    | Frequency | **Daily** |
    | Time | **12:00 AM** |
    | Timezone | the name of your local time zone |
    | Retain instant recovery snapshot(s) for | **2** Days(s) |

1. Click **OK** to create the policy and then, in the **Virtual Machines** section, select **Add**.

    >You can create multiple backup policies or reuse a single backup policy on multiple virtual machines. 

1. On the **Select virtual machines** blade, select **vm1**, click **OK**.

1. On the **Backup** blade, click **Enable backup**.

    >Wait for the backup to be enabled. This should take approximately 2 minutes.

1. In the **Protected items** section, click **Backup items**, and then click the **Azure virtual machine** entry.

1. Select the **View details** link for **vm1**, and review the values of the **Backup Pre-Check** and **Last Backup Status** entries.

    >Notice the backup is pending.
    
1. Select **Backup now**, accept the default value in the **Retain Backup Till** drop-down list, and click **OK**. Do not wait for the backup to complete.

    >**Check your learning**
    + Do you know the difference between an Enhanced and Standard backup policy?
    + Can you configure backup policy retention settings?
    + Can you review the backup job details and status?

## Learn more with self-paced training

+ [Protect your virtual machines by using Azure Backup](https://learn.microsoft.com/training/modules/protect-virtual-machines-with-azure-backup/). Use Azure Backup to help protect on-premises servers, virtual machines, SQL Server, Azure file shares, and other workloads.

## Key takeaways

Congratulations on completing the lab. Here are the main takeaways for this lab. 

+ A Recovery Services vault stores your backup data and minimizes management overhead.
+ Azure Backup service provides simple, secure, and cost-effective solutions to back up and recover your data.
+ Azure Backup can protect on-premises and cloud resources including virtual machines and file shares.
+ Azure Backup policies configure the frequency of backups and the retention period for recovery points. 






