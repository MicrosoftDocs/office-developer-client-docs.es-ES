---
title: Los límites de un conjunto de registros
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e13e907c27fa6f764aae6ee499f0bd2854f9640b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483611"
---
# <a name="the-limits-of-a-recordset"></a>Los límites de un conjunto de registros


**Se aplica a**: Access 2013 | Office 2013

Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se han sobrepasado los límites de un objeto **Recordset** al moverse de un registro a otro. Considere **BOF** y **EOF** como registros "fantasma" situados al principio y al final del **conjunto de registros**. Trabajando con el **conjunto de registros** de ejemplo de [Examinar datos](chapter-3-examining-data.md), ahora tendría este aspecto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>ProductName</p></th>
<th><p>UnitPrice (PrecioUnitario)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>Peras secas orgánicas del tío Bob</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>Cuajada de judías</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Col fermentada Rössle</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Manzanas secas Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Queso de soja Longlife</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


La propiedad **BOF** devuelve **True** (-1) si la posición del registro activo es anterior al primer registro y **False** (0) si la posición del registro activo está en el primer registro o después de él.

La propiedad **EOF** devuelve **True** si la posición del registro activo es posterior al último registro y **False** si la posición del registro activo está en el último registro o antes de él.

Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro activo, como se muestra en el código siguiente:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

Si se abre un objeto **Recordset** que no contiene ningún registro, las propiedades **BOF** y **EOF** se establecen en **True** y el valor de la propiedad **RecordCount** del objeto **Recordset** dependerá del tipo de cursor. para los cursores dinámicos, se devolverá -1 (**CursorType** = **adOpenDynamic**) y, para otros cursores, se devolverá 0.

Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el activo y las propiedades **BOF** y **EOF** son **False**.

Si se elimina el último registro que queda en el objeto **Recordset**, el cursor queda en un estado indeterminado. Las propiedades **BOF** y **EOF** pueden permanecer en **False** hasta que se intente ajustar la posición del registro activo, dependiendo del proveedor.

