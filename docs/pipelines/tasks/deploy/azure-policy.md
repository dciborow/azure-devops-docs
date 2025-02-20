---
title: Azure Policy task 
description: Security and compliance assessment with Azure policies
ms.assetid: 80CE5090-EF14-4640-A833-5C43271FB6EA
ms.topic: reference
ms.custom: seodec18
ms.author: ronai
author: RoopeshNair
ms.date: 03/12/2019
monikerRange: '> tfs-2018'
---

# Security and Compliance Assessment task

[!INCLUDE [version-gt-eq-2019](../../../includes/version-gt-eq-2019.md)]

[Azure Policy](/azure/governance/policy/) allows you to assess and enforce resource compliance against defined IT policies.
Use this task in a gate to identify, analyze and evaluate the security risks,
and determine the mitigation measures required to reduce the risks.

## Demands

Can be used only as a [gate](../../release/approvals/gates.md).
This task is not supported in a build or release pipeline.

![Using the task as a gate in a release pipeline](media/gates.png)

::: moniker range="> tfs-2018"

## YAML snippet

[!INCLUDE [temp](../includes/yaml/AzurePolicyV0.md)]

> [!IMPORTANT]
> Service connections cannot be specified by variable.

::: moniker-end

## Arguments

<table><thead><tr><th>Parameters</th><th>Description</th></tr></thead>
<tr><td>Azure subscription<td>(Required) Select the Azure Resource Manager subscription on which to enforce the policies.</td></tr>
<tr><td>Resource group</td><td>Select the Resource Group or specify a variable name.</td></tr>
<tr><td>Resource name</td><td>Select the name of the Azure resources for which you want to check policy compliance.</td></tr>
</table>