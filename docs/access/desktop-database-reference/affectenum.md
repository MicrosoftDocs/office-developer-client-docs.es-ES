---
title: AffectEnum (referencia de base de datos de escritorio de Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297203"
---
# <a name="affectenum"></a>AffectEnum

**Se aplica a:** Access 2013, Office 2013

Especifica a qué registros afecta una operación.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3 </p></td>
<td><p>Si no existe ninguna propiedad <a href="filter-property-ado.md">Filter</a> aplicada al objeto <strong>Recordset</strong>, afecta a todos los registros. Si la <strong>propiedad Filter</strong> se establece en un criterio de cadena (como Author='Smith'), la operación afecta a los registros &quot; &quot; visibles del capítulo actual. Si la <strong>propiedad Filter</strong> se establece en un miembro de <a href="filtergroupenum.md">FilterGroupEnum</a> o una matriz de marcadores, la operación afectará a todas las filas del conjunto de <strong>registros</strong>.</p><p><strong>NOTA:</strong>adAffectAll está oculto en el explorador Visual Basic objetos.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4 </p></td>
<td><p>Afecta a todos los registros de todos los capítulos secundarios del <strong>Recordset</strong>, incluidos aquellos no visibles a través de ningún <strong>Filtro</strong> aplicado actualmente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1 </p></td>
<td><p>Afecta sólo al registro actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2 </p></td>
<td><p>Afecta únicamente a los registros que cumplen el valor actual de la propiedad <a href="filter-property-ado.md">Filter</a>. Para usar esta opción, debe establecer la propiedad <strong>Filter</strong> en un valor <strong>FilterGroupEnum</strong> o en una matriz de <strong>marcadores</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente a ADO/WFC

Paquete: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

