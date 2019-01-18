---
title: Hierarchy (objeto, ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726046"
---
# <a name="hierarchy-object-ado-md"></a>Hierarchy (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Representa una forma de agregar o "acumular" los miembros de una [dimensión](dimension-object-ado-md.md). Una dimensión se puede agregar a una o varias jerarquías.

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **Hierarchy**, puede hacer lo siguiente:

  - Identificar la **jerarquía** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).

  - Devolver una cadena que describa la **jerarquía** con la propiedad [Description](description-property-ado-md.md).

  - Devolver los objetos [Level](level-object-ado-md.md) que componen la **jerarquía** con la colección [Levels](levels-collection-ado-md.md).

  - Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Hierarchy**.

La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AllMember</p></td>
<td><p>Miembro del nivel superior de resumen de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>NombreCatálogo</p></td>
<td><p>Nombre del catálogo al que pertenece el cubo.</p></td>
</tr>
<tr class="odd">
<td><p>Nombre de cubo</p></td>
<td><p>Nombre del cubo.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Nombre único del miembro predeterminado de la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Descripción de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Tipo de dimensión al que pertenece esta jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Nombre inequívoco de la dimensión.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Etiqueta o título asociado a la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>Número de miembros de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>GUID de la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyName</p></td>
<td><p>Nombre de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Nombre inequívoco de la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Nombre del esquema al que pertenece el cubo.</p></td>
</tr>
</tbody>
</table>

