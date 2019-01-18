---
title: Dimension (objeto, ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712830"
---
# <a name="dimension-object-ado-md"></a>Dimension (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Representa una de las dimensiones de un cubo multidimensional, que contiene una o más jerarquías de elementos.

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **Dimension**, puede hacer lo siguiente:

  - Identificar la **dimensión** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).

  - Devolver una cadena que describa la **dimensión** con la propiedad [Description](description-property-ado-md.md).

  - Devolver los objetos [Hierarchy](hierarchy-object-ado-md.md) que componen la **dimensión** con la colección [Hierarchies](hierarchies-collection-ado-md.md).

  - Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Dimension**.

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
<td><p>NombreCatálogo</p></td>
<td><p>Nombre del catálogo al que pertenece el cubo.</p></td>
</tr>
<tr class="even">
<td><p>Nombre de cubo</p></td>
<td><p>Nombre del cubo.</p></td>
</tr>
<tr class="odd">
<td><p>DefaultHierarchy</p></td>
<td><p>Nombre único de la jerarquía predeterminada.</p></td>
</tr>
<tr class="even">
<td><p>Description</p></td>
<td><p>Descripción del cubo.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Etiqueta o título asociado a la dimensión.</p></td>
</tr>
<tr class="even">
<td><p>DimensionCardinality</p></td>
<td><p>Número de miembros de la dimensión.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>GUID de la dimensión.</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>Nombre de la dimensión.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>Número ordinal de la dimensión entre el grupo de dimensiones que forman el cubo.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Tipo de dimensión.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Nombre inequívoco de la dimensión.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Nombre del esquema al que pertenece el cubo.</p></td>
</tr>
</tbody>
</table>

