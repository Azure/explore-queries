# Azure Infrastructure Exploration Queries

Welcome to **Azure VM Exploration Queries**, a collection of flexible [Azure Resource Graph (ARG)](https://learn.microsoft.com/azure/governance/resource-graph/overview) queries designed to help IT professionals rapidly "size up" and analyze [VM-based Azure environments](https://learn.microsoft.com/azure/virtual-machines/overview) based on specific workloads. This repository includes a series of [Kusto Query Language (KQL)](https://learn.microsoft.com/kusto/query) queries that let you group virtual machines (VMs) according to naming conventions, [tags](https://learn.microsoft.com/azure/azure-resource-manager/management/tag-resources), [resource groups](https://learn.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal#what-is-a-resource-group), and more, giving you insights into VM inventory, SKU usage, [VM Scale Sets (VMSS)](https://learn.microsoft.com/azure/virtual-machine-scale-sets/overview), and [availability zone](https://learn.microsoft.com/azure/reliability/availability-zones-overview?tabs=azure-cli) distribution.

## Overview

Each query in this repository is structured to support easy and customizable VM grouping. Simply read the **commented "Grouping Options" section** in each query, select the option that best fits your environment, and uncomment the relevant line(s). This flexible approach makes it easy to tailor analyses to your specific needs, whether you’re working with small applications or complex, multi-tier workloads.

## Queries Included

| Query File                 | Description                                                                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**vm_group_inventory.kql**](queries/vm_group_inventory.kql) | Provides a full inventory of VMs grouped by your chosen method. This query helps you understand how VMs are distributed across your environment, giving you an overview of each group’s VM count and resource allocation. |
| [**vm_group_sku_analysis.kql**](queries/vm_group_sku_analysis.kql) | Analyzes the VM SKUs within each group, allowing you to assess resource allocation, identify cost implications, and optimize SKU usage based on workload requirements. |
| [**vm_group_vmss_analysis.kql**](queries/vm_group_vmss_analysis.kql) | Examines VM Scale Sets (VMSS) associated with each group, offering insights into scalability and deployment configurations for each workload. |
| [**vm_group_zone_analysis.kql**](queries/vm_group_zone_analysis.kql) | Evaluates the distribution of VMs across availability zones within each group, providing insights into redundancy, fault tolerance, and geographic placement. |

## How to Use

1. **Choose Your Grouping Option**: Each query includes a "Grouping Options" section with multiple methods for grouping VMs (e.g., by name prefix, custom regex pattern, resource group, or tag). Review the comments in this section, choose the option that best matches your environment, and uncomment the relevant line(s).
  
2. **Customize If Needed**: For some options, such as regex patterns or specific tags, you may need to adjust values to fit your organization’s conventions. Use Copilot or other tools to build regex patterns quickly if needed.

3. **Run the Query**: Once you’ve configured the grouping, run the query in Azure Resource Graph Explorer to get a detailed view of VM distribution, SKU usage, or zone alignment based on your configuration.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
