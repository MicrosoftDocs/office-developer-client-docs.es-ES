---
title: Member (objeto) (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289425"
---
# <a name="member-object-ado-md"></a>Member (objeto) (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Representa un miembro de un nivel en un cubo, los miembros secundarios de un miembro de un nivel o un miembro de una posición a lo largo de un eje de un conjunto de celdas.

## <a name="remarks"></a>Comentarios

Las propiedades de un **miembro** difieren en función del contexto en el que se utilice. Un **miembro** de un [nivel](level-object-ado-md.md) en un objeto [CubeDef](cubedef-object-ado-md.md) tiene una propiedad [Children](children-property-ado-md.md) que devuelve los **miembros** del siguiente nivel inferior de la jerarquía del **miembro** actual. Para un **miembro** de una [posición](position-object-ado-md.md), la colección **Children** siempre está vacía. Además, la propiedad [Type](type-property-ado-md.md) sólo se aplica a los **miembros** de un **nivel**.

Un **miembro** de una **posición** tiene dos propiedades ( [DrilledDown](drilleddown-property-ado-md.md) y [ParentSameAsPrev](parentsameasprev-property-ado-md.md) ) que se usan al mostrar el [conjunto de celdas](cellset-object-ado-md.md). Se producirá un error si se obtiene acceso a estas propiedades en un **miembro** de un **nivel**.

Con las colecciones y las propiedades de un objeto **Member** de un **nivel**, puede hacer lo siguiente:

  - Identificar el **miembro** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).

  - Devolver una cadena para utilizarla al mostrar el **miembro** con la propiedad [Caption](caption-property-ado-md.md).

  - Devolver una cadena que describa un **miembro** de medida o fórmula con la propiedad [Description](description-property-ado-md.md).

  - Determinar la naturaleza del **miembro** con la propiedad [Type](type-property-ado-md.md).

  - Obtener información sobre el **nivel** del **miembro** con las propiedades [LevelDepth](leveldepth-property-ado-md.md) y [LevelName](levelname-property-ado-md.md).

  - Obtener **miembros** relacionados en una [jerarquía](hierarchy-object-ado-md.md) con las propiedades [Parent](parent-property-ado-md.md) y [Children](children-property-ado-md.md).

  - Contar los miembros secundarios de un **miembro** con la propiedad [ChildCount](childcount-property-ado-md.md).

  - Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Level**.

Con las colecciones y las propiedades de un objeto **Member** de una **posición** a lo largo de un [eje](axis-object-ado-md.md), puede hacer lo siguiente:

  - Identificar el **miembro** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).

  - Devolver una cadena para utilizarla al mostrar el **miembro** con la propiedad [Caption](caption-property-ado-md.md).

  - Devolver una cadena que describa un **miembro** de medida o fórmula con la propiedad [Description](description-property-ado-md.md).

  - Obtener información sobre el **nivel** del **miembro** con las propiedades [LevelDepth](leveldepth-property-ado-md.md) y [LevelName](levelname-property-ado-md.md).

  - Contar los miembros secundarios de un **miembro** con la propiedad [ChildCount](childcount-property-ado-md.md).

  - Utilizar la propiedad [DrilledDown](drilleddown-property-ado-md.md) para determinar si hay al menos un miembro secundario en el **eje** inmediatamente detrás de este **miembro**.

  - Utilizar la propiedad [ParentSameAsPrev](parentsameasprev-property-ado-md.md) para determinar si el miembro principal de este **miembro** es el mismo que el miembro principal del **miembro** inmediatamente anterior.

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
<td><p>ChildrenCardinality</p></td>
<td><p>Número de miembros secundarios que tiene el miembro.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Nombre del cubo.</p></td>
</tr>
<tr class="even">
<td><p>Descripción</p></td>
<td><p>Descripción del miembro.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Nombre inequívoco de la <a href="dimension-object-ado-md.md">dimensión</a>.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Nombre inequívoco de la jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>Distancia entre el nivel y la raíz de la jerarquía.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Nombre inequívoco del nivel.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Etiqueta o título asociado al miembro.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>GUID del miembro.</p></td>
</tr>
<tr class="odd">
<td><p>Nombrede miembro</p></td>
<td><p>Nombre del miembro.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>Número ordinal del miembro.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>Tipo de miembro.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>Nombre inequívoco del miembro.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>Número de miembros principales que tiene el miembro.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>Número de nivel del miembro principal.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>Nombre inequívoco del miembro principal.</p></td>
</tr>
<tr class="even">
<td><p>Equivale</p></td>
<td><p>Nombre del esquema al que pertenece el cubo.</p></td>
</tr>
</tbody>
</table>

