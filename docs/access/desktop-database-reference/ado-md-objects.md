---
title: Objetos de ADO MD (referencia de escritorio de la base de datos de Access)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bde8dfebd4351275ede6e08cbeec7d8e3d710c3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485364"
---
# <a name="ado-md-objects"></a>Objetos de ADO MD


**Se aplica a**: Access 2013 | Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Eje</a></p></td>
<td><p>Representa un eje de posición o de filtro de un conjunto de celdas, que contiene elementos seleccionados de una o más dimensiones.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Catálogo</a></p></td>
<td><p>Contiene información de esquema multidimensional (es decir, cubos y dimensiones subyacentes, jerarquías, niveles y elementos) específica de un proveedor de datos multidimensionales (MDP).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Representa los datos de la intersección de coordenadas de ejes, contenidos en un conjunto de celdas.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Conjunto de celdas</a></p></td>
<td><p>Representa los resultados de una consulta multidimensional. Es un conjunto de celdas seleccionadas de cubos u otro conjuntos de celdas.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">Objeto CubeDef</a></p></td>
<td><p>Representa un cubo de un esquema multidimensional, que contiene un conjunto de dimensiones relacionadas.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimensión</a></p></td>
<td><p>Representa una de las dimensiones de un cubo multidimensional, que contiene una o más jerarquías de elementos.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Jerarquía</a></p></td>
<td><p>Representa una forma en que se pueden agregar los miembros de una dimensión o &quot;resumidas. &quot; Una dimensión se puede agregar a lo largo de una o varias jerarquías.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Contiene un conjunto de miembros que tienen el mismo rango dentro de una jerarquía.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Elemento</a></p></td>
<td><p>Representa un miembro de un nivel en un cubo, los miembros secundarios de un miembro de un nivel o un miembro de una posición a lo largo de un eje de un conjunto de celdas.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Representa un conjunto de uno o varios miembros de dimensiones diferentes, que define un punto a lo largo de un eje.</p></td>
</tr>
</tbody>
</table>


Además, el objeto **Catalog** está conectado a un objeto **Connection** de ADO, que se incluye con la biblioteca estándar de ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p>Representa una conexión abierta con un origen de datos.</p></td>
</tr>
</tbody>
</table>


Una colección puede contener numerosos objetos de ADO MD. Por ejemplo, un objeto [CubeDef](cubedef-object-ado-md.md) puede estar contenido en una colección [CubeDefs](cubedefs-collection-ado-md.md) de un **catálogo**. Para obtener más información, vea [Colecciones de ADO MD](ado-md-collections.md).

