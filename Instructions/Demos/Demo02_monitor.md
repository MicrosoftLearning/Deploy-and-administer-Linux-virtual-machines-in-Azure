---
demo:
    title: 'Demo 02: Monitor virtual machines'
    module: 'Guided Project: Deploy and administer Linux virtual machines'
---

# Demo 02: Monitor virtual machines

## Credential tasks

+ Create a virtual machine (Quickstart template).
+ Configure VM Insights.
+ Create an alert.  
+ Identify performance issues. 
+ Resize a virtual machine. 

## Resource requirements

+ Linux virtual machine (create using a custom template)

## Reference slides 

+ Azure Resource Manager templates
+ Azure Monitor key capabilities
+ Azure Monitor components
+ Metrics and logs

  
## Reference steps

Detailed steps are provided in these links.

+ [Deploy a simple Ubuntu Linux VM](https://learn.microsoft.com/azure/virtual-machines/linux/quick-create-template)
+ [Enable VM insights for Azure Monitor Agent](https://learn.microsoft.com/azure/azure-monitor/vm/vminsights-enable-portal#enable-vm-insights-for-azure-monitor-agent) 
+ [Tutorial: Create a metric alert for an Azure resource](https://learn.microsoft.com/azure/azure-monitor/alerts/alerts-create-metric-alert-rule)


## Reference slides (optional)

Use these slides for additional context.



## Discussion points

1. Use **Deploy a custom template** for a simple Linux Ubuntu machine. This is how the students will create the VM in the exercise. Discuss the use of templates. 

1. Enable VM Insights. Review how to use a data collection rule and how to select a Log Analytics workspace. 

1. Create an alert based on metrics. For example, create a new alert rule based on CPU percentage usage.

1. Discuss the use of action groups and how to assign an action group to the alert. 

1. Review how to monitor an alert when it is triggered.

1. Close with how to export the resource template. 
