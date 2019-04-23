---
title: Propiedades dinámicas de ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281718"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="069bd-102">Propiedades dinámicas de ADO</span><span class="sxs-lookup"><span data-stu-id="069bd-102">ADO dynamic properties</span></span>

<span data-ttu-id="069bd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="069bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="069bd-p101">Las propiedades dinámicas se pueden agregar a las colecciones [Properties](properties-collection-ado.md) de los objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) o [Recordset](recordset-object-ado.md). El origen de estas propiedades es un proveedor de datos, tal como el [Proveedor OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), o un proveedor de servicios, tal como el [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte la documentación correspondiente del proveedor de datos o servicios para obtener más información acerca de una propiedad dinámica concreta.</span><span class="sxs-lookup"><span data-stu-id="069bd-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="069bd-107">El [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) proporciona una referencia cruzada entre los nombres ADO y OLE DB para cada propiedad dinámica estándar del proveedor OLE DB.</span><span class="sxs-lookup"><span data-stu-id="069bd-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="069bd-p102">Las siguientes propiedades dinámicas son de interés especial, y también aparecen documentadas en los orígenes antes mencionados. La funcionalidad especial con ADO se documenta en los tema de Ayuda de ADO enumerados a continuación.</span><span class="sxs-lookup"><span data-stu-id="069bd-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="069bd-110">Propiedad Dynamic</span><span class="sxs-lookup"><span data-stu-id="069bd-110">Dynamic property</span></span></th>
<th><span data-ttu-id="069bd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="069bd-111">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="069bd-112"><a href="optimize-property-dynamic-ado.md">Optimizar</a></span><span class="sxs-lookup"><span data-stu-id="069bd-112"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-113">Especifica si se debe crear un índice sobre este campo.</span><span class="sxs-lookup"><span data-stu-id="069bd-113">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="069bd-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="069bd-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-115">Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</span><span class="sxs-lookup"><span data-stu-id="069bd-115">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="069bd-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="069bd-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-117">Especifica un nombre para el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="069bd-117">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="069bd-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="069bd-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-119">Especifica una cadena de comando proporcionada por el usuario que el método <strong>Resync</strong> emite para actualizar los datos de la tabla especificada en la propiedad dinámica <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="069bd-119">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="069bd-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="069bd-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-121"><strong>Unique Table</strong> : especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="069bd-121"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span><br/><br/><span data-ttu-id="069bd-122"><strong>Unique Schema</strong> : especifica el esquema o el nombre del propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="069bd-122"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span><br/><br/><span data-ttu-id="069bd-123"><strong>Unique Catalog</strong> — especifica el catálogo o el nombre de la base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="069bd-123"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="069bd-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="069bd-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="069bd-125">Especifica si el método <strong>UpdateBatch</strong> va seguido de una operación implícita del método <strong>Resync</strong> y, en ese caso, el ámbito de esa operación.</span><span class="sxs-lookup"><span data-stu-id="069bd-125">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

