﻿---
title: Disconnect organization from Azure AD
titleSuffix: Azure DevOps Services
ms.custom: seodec18
description: Learn how to stop using your organization's Azure AD and sign in with a Microsoft account by disconnecting your organization from your directory
ms.technology: devops-accounts
ms.assetid: 3eb744cf-854d-4cbd-b725-c2e070bd922b
ms.topic: conceptual
ms.author: chcomley
author: chcomley
ms.date: 05/14/2019
monikerRange: 'azure-devops'
---
# Disconnect your organization from Azure Active Directory

[!INCLUDE [version-eq-azure-devops](../../includes/version-eq-azure-devops.md)]

<a name="DisconnectDirectory"></a>

To stop using your organization's Azure Active Directory (Azure AD) and return to signing in with Microsoft accounts, disconnect your organization from your directory.

For more information about using Azure AD with Azure DevOps, see the [conceptual overview](access-with-azure-ad.md).

## Prerequisites

* Before you disconnect your organization from your directory, make sure to **change the organization Owner to a Microsoft account** and not to a school or work account. You can't sign in to your organization unless your work or school account has the same email address as your Microsoft account.

* Add your Microsoft account to the Project Collection Administrator group in Organization Settings and confirm that you have Global Administrator Permissions in your Azure AD for your Microsoft account. You need both because Azure AD users can't disconnect organizations from directories. You can add Microsoft accounts to a directory as external users.

Learn about how to [Manage Azure administrators](/azure/active-directory/users-groups-roles/directory-assign-admin-roles).

**What happens to current users?**  Users can migrate everything except work history. They can reconnect Visual Studio subscriptions and have their access levels reassigned to their new identities.

> [!IMPORTANT]
> If you want to connect your organization to a different Azure Active Directory at any time, ensure that any connected organizations are disconnected from the original directory BEFORE you delete that directory. Once a new directory is established, connect your organization to the new directory so users can regain access. Learn more about [connecting your organization to Azure AD](connect-organization-to-azure-ad.md).

## Disconnect organization from directory

1. Sign in to your organization (```https://dev.azure.com/{yourorganization}```).

2. Select ![gear icon](../../media/icons/gear-icon.png) **Organization settings**.

    ![Open Organization settings](../../media/settings/open-admin-settings-vert.png)

3. Select **Azure Active Directory**, and then select **Disconnect directory**.

   ![Organization settings, disconnect directory](media/shared/select-disconnect-directory.png)

4. Enter the name of your organization, and then select **Disconnect**.

   ![Disconnection confirmation](media/shared/disconnection-confirmation.png)

5. Select **Sign out**.

   ![Select Sign out](media/shared/sign-out-azure-devops.png)

Your organization is disconnected from Azure AD. Only users with Microsoft accounts can sign in.

For answers to frequently asked questions about connecting to, disconnecting from, or switching your Azure AD, see [FAQs](./faq-azure-access.yml#faq-connect).

## Related articles

* [Connect your organization to Azure Active Directory](connect-organization-to-azure-ad.md)
* [About access with Azure AD](access-with-azure-ad.md)
* [Get a list of organizations backed by Azure AD](get-list-of-organizations-connected-to-azure-active-directory.md)
* [Restrict organization creation with tenant policy](azure-ad-tenant-policy-restrict-org-creation.md)
* [Frequently asked questions (FAQs) about connecting, disconnecting, or changing your Azure AD](./faq-azure-access.yml#connect-to-disconnect-from-or-change-azure-ad-connection)