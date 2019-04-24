---
title: LEVEL (objeto) (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290117"
---
# <a name="level-object-ado-md"></a>LEVEL (objeto) (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Contiene un conjunto de miembros que tienen el mismo rango dentro de una jerarquía.

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **Level**, puede hacer lo siguiente:

  - Identificar el **nivel** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).

  - Devolver una cadena para utilizarla al mostrar el **nivel** con la propiedad [Caption](caption-property-ado-md.md).

  - Devolver una cadena que describa el **nivel** con la propiedad [Description](description-property-ado-md.md).

  - Devolver los objetos [Member](member-object-ado-md.md) que componen el **nivel** con la colección [Members](members-collection-ado-md.md).

  - Devolver el número de niveles de la raíz del **nivel** con la propiedad [Depth](depth-property-ado-md.md).

  - Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Level**.

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
<td><p>Nombrecatálogo</p></td>
<td><p>Nombre del catálogo al que pertenece el cubo.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Nombre del cubo.</p></td>
</tr>
<tr class="odd">
<td><p>Descripción</p></td>
<td><p>Descripción del nivel.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Nombre inequívoco de la <a href="dimension-object-ado-md.md">dimensión</a>.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>Nombre inequívoco de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Etiqueta o título asociado al nivel.</p></td>
</tr>
<tr class="odd">
<td><p>LevelCardinality</p></td>
<td><p>Número de miembros del nivel.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>GUID del nivel.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Nombre del nivel.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>Distancia entre el nivel y la raíz de la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>Tipo de nivel.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Nombre inequívoco del nivel.</p></td>
</tr>
<tr class="odd">
<td><p>Equivale</p></td>
<td><p>Nombre del esquema al que pertenece el cubo.</p></td>
</tr>
</tbody>
</table>

