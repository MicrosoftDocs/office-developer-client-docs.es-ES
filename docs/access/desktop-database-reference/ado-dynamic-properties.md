---
title: Propiedades dinámicas de ADO
TOCTitle: ADO Dynamic Properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a35bf0cd62db8f635540bfd1ccd65995b198b46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877551"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="2d8c2-102">Propiedades dinámicas de ADO</span><span class="sxs-lookup"><span data-stu-id="2d8c2-102">ADO Dynamic Properties</span></span>


<span data-ttu-id="2d8c2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d8c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d8c2-p101">Las propiedades dinámicas se pueden agregar a las colecciones [Properties](properties-collection-ado.md) de los objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) o [Recordset](recordset-object-ado.md). El origen de estas propiedades es un proveedor de datos, tal como el [Proveedor OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), o un proveedor de servicios, tal como el [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte la documentación correspondiente del proveedor de datos o servicios para obtener más información acerca de una propiedad dinámica concreta.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="2d8c2-107">El [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) proporciona una referencia cruzada entre los nombres ADO y OLE DB para cada propiedad dinámica estándar del proveedor OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="2d8c2-p102">Las siguientes propiedades dinámicas son de interés especial, y también aparecen documentadas en los orígenes antes mencionados. La funcionalidad especial con ADO se documenta en los tema de Ayuda de ADO enumerados a continuación.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d8c2-110"><a href="optimize-property-dynamic-ado.md">Optimizar</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-110"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-111">Especifica si se debe crear un índice sobre este campo.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-111">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8c2-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-113">Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-113">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8c2-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-115">Especifica un nombre para el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-115">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8c2-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-117">Especifica una cadena de comando proporcionada por el usuario que el método <strong>Resync</strong> emite para actualizar los datos de la tabla especificada en la propiedad dinámica <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-117">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8c2-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-119"><strong>Unique Table</strong> — especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-119"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span> <span data-ttu-id="2d8c2-120"><strong>Unique Schema</strong> — especifica el esquema o el nombre del propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-120"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span> <span data-ttu-id="2d8c2-121"><strong>Unique Catalog</strong> — especifica el catálogo o el nombre de la base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-121"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8c2-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="2d8c2-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="2d8c2-123">Especifica si el método <strong>UpdateBatch</strong> es seguido por una operación implícita del método <strong>Resync</strong> y, si es así, el ámbito de esa operación.</span><span class="sxs-lookup"><span data-stu-id="2d8c2-123">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

