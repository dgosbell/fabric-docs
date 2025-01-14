---
title: Create an Eventhouse (preview)
description: Learn about how to create an Eventhouse for data storage in Real-Time Analytics.
ms.reviewer: sharmaanshul
ms.author: yaschust
author: YaelSchuster
ms.topic: how-to
ms.date: 02/08/2024
ms.search.form: Eventhouse
---
# Create and manage an Eventhouse (preview)

An Eventhouse allows you to manage multiple databases at once, sharing capacity and resources to optimize performance and cost. It provides unified monitoring and management across all databases and per database. For more information, see [Eventhouse overview (preview)](eventhouse.md).

[!INCLUDE [feature-preview-note](../includes/feature-preview-note.md)]

In this article, you learn how to create an Eventhouse, add new databases to an Eventhouse, and delete an Eventhouse.

## Prerequisites

* A [workspace](../get-started/create-workspaces.md) with a Microsoft Fabric-enabled [capacity](../enterprise/licenses.md#capacity)

## Enable tenant settings in the admin portal

> [!IMPORTANT]
> This step must be completed by the tenant admin.

1. Browse to the [admin portal](../admin/admin-center.md).
1. In the **Tenant settings** tab, search for *Eventhouse*. For more information, see [About tenant settings](../admin/about-tenant-settings.md).
1. Toggle the button for **Create Eventhouse (preview)** to **Enabled**. For more information, see [Tenant settings - Microsoft Fabric](../admin/tenant-settings-index.md).
1. Select **Apply**. 

    :::image type="content" source="media/eventhouse/enable-admin-settings.png" alt-text="Screenshot of section of admin settings relating to enabling Eventhouse.":::

## Create an Eventhouse

1. Browse to your workspace homepage in Real-Time Analytics.
1. Select **New** > **Eventhouse**.

    :::image type="content" source="media/eventhouse/new-eventhouse.png" alt-text="Screenshot of creating new Eventhouse item in Real-Time Analytics.":::

1. Enter a name for the Eventhouse. Both an Eventhouse and its default child KQL database are created with the same name. The database name, like all items in Fabric, can be renamed at any time.

    > [!NOTE]
    > The Eventhouse name can contain alphanumeric characters, underscores, periods, and hyphens. Special characters aren't supported.

    :::image type="content" source="media/eventhouse/create-eventhouse.png" alt-text="Screenshot of creating Eventhouse by entering name in Real-Time Analytics." lightbox="media/eventhouse/create-eventhouse.png":::

1. The [database details](create-database.md#database-details) page opens for the default database in the newly created Eventhouse. To view all the databases in this Eventhouse or create new databases, select the **Eventhouse** menu item.

    :::image type="content" source="media/eventhouse/choose-eventhouse.png" alt-text="Screenshot of choosing Eventhouse from database details page." lightbox="media/eventhouse/choose-eventhouse.png":::

## View all databases in an Eventhouse

1. From the Eventhouse pane, select **Browse all databases**. Alternatively, select the Eventhouse item from your list of items in the workspace.

    :::image type="content" source="media/eventhouse/browse-databases.png" alt-text="Screenshot of Eventhouse pane with Browse all databases highlighted in a red box.":::'

    A window opens with details about all the databases in this Eventhouse.

    :::image type="content" source="media/eventhouse/browse-all-databases.png" alt-text="Screenshot of database view in Eventhouse in Real-Time Analytics.":::

1. Toggle between list and tile view using the buttons on the top right of the page.

    :::image type="content" source="media/eventhouse/list-tile-view.png" alt-text="Screenshot showing the Eventhouse details page with the tile and list view buttons surrounded by a red box.":::

1. To explore a specific database, select the name of this database from the list.

## Add a KQL database to an existing Eventhouse

In this section, you add a new KQL database to an existing Eventhouse. This database can be either a standard KQL database or a [database shortcut](database-shortcut.md).

1. Select the Eventhouse from your list of items in the workspace.
1. Select **New database +**.

    :::image type="content" source="media/eventhouse/new-database.png" alt-text="Screenshot showing the databases summary in Eventhouse.":::

1. Enter a database name, and select **Create**.

## Enable minimum consumption

[Minimum consumption](eventhouse.md#minimum-consumption) sets a minimum available capacity unit (CU) size for your Eventhouse.



1. Select the Eventhouse from your list of items in the workspace.
1. In the top righthand side of the Eventhouse details page, select **Eventhouse settings** > **Minimum consumption**
1. From the dropdown, select the size corresponding to the [minimium available CU](eventhouse.md#minimum-consumption) size you want to apply to this Eventhouse.

    The following table maps the size to the minimum [capacity units](../admin/service-admin-portal-capacity-settings.md) allotted to the Eventhouse:
    
    | Name        | Minimum CUs|
    |-------------|------------|
    | Extra Small | 8.5        |
    | Small       | 13         |
    | Medium      | 18         |
    | Large       | 26         |
    | Extra Large | 34         |
    | 2X Large    | 56         |

    :::image type="content" source="media/eventhouse/guaranteed-availability.png" alt-text="Screenshot showing how to select the correct minimum consumption in Real-Time Analytics Eventhouse."  lightbox="media/eventhouse/guaranteed-availability.png":::


## Delete an Eventhouse

When you delete an Eventhouse, both the Eventhouse and all its child KQL databases are deleted forever.

1. Browse to the Eventhouse item in your workspace.
1. Select **More menu** [**...**] > **Delete**.

    :::image type="content" source="media/eventhouse/delete-eventhouse.png" alt-text="Screenshot of deleting Eventhouse.":::

## Related content

* [Eventhouse overview (Preview)](eventhouse.md)
* [Create a KQL database](create-database.md)