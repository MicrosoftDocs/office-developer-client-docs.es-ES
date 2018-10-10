---
title: Relation Members (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d8395425f10f12d515956a07cd9a190d3544527
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485796"
---
# <a name="relation-members-dao"></a><span data-ttu-id="bb768-102">Relation Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb768-102">Relation Members (DAO)</span></span>


<span data-ttu-id="bb768-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb768-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bb768-104">Un objeto Relation representa una relación entre campos de tablas o consultas (sólo bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bb768-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="bb768-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb768-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb768-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb768-106">Name</span></span></p></th>
<th><p><span data-ttu-id="bb768-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb768-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb768-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-109">Crea un nuevo objeto <strong><a href="field-object-dao.md">Field</a></strong> (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bb768-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="bb768-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb768-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb768-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb768-111">Name</span></span></p></th>
<th><p><span data-ttu-id="bb768-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb768-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb768-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p101">Establece o devuelve un valor que indica una o varias características del objeto <strong>Relation</strong>. <strong>Long</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bb768-p101">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb768-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p102">Devuelve una colección <strong>Fields</strong> que representa todos los objetos <strong>Field</strong> almacenados para el objeto especificado. Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb768-p102">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb768-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p103">Establece o devuelve el nombre de la tabla externa en una relación (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bb768-p103">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb768-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p104">Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</span><span class="sxs-lookup"><span data-stu-id="bb768-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb768-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p105">Establece o devuelve un valor en un objeto <strong>Relation</strong> que indica si esa relación se debería tener en cuenta al rellenar una réplica parcial desde una réplica completa. (Sólo para base de datos del motor de base de datos Microsoft Access). <strong>Boolean</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bb768-p105">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb768-130"><strong><a href="relation-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p106">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb768-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb768-133"><strong><a href="relation-table-property-dao.md">Tabla</a></strong></span><span class="sxs-lookup"><span data-stu-id="bb768-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bb768-p107">Indica el nombre de la tabla principal de un objeto <strong><a href="relation-object-dao.md">Relation</a></strong>. El resultado debe ser el mismo que el valor de la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> de un objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> o <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bb768-p107">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table. This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

