---
title: UpdateCriteriaEnum Enumeration (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dc671458d53f6e40e27ff2dd338f010c09dc5ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484428"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>UpdateCriteriaEnum Enumeration (DAO)


**Se aplica a**: Access 2013 | Office 2013

Se utiliza con el método **UpdateOptions** para especificar cómo se crea una actualización por lotes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbCriteriaAllCols</p></td>
<td><p>4</p></td>
<td><p>Utiliza la columna o columnas de clave y todas las columnas en la cláusula WHERE.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16</p></td>
<td><p>Utiliza un par de instrucciones DELETE e INSERT para cada fila modificada.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1</p></td>
<td><p>Utiliza sólo la columna o columnas de clave en la cláusula WHERE.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2</p></td>
<td><p>Utiliza la columna o columnas de clave y todas las columnas actualizadas en la cláusula WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8</p></td>
<td><p>Utiliza sólo la columna de marcas de hora si está disponible (se generará un error en tiempo de ejecución si no hay ninguna columna de marcas de hora en el conjunto de resultados).</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>Utiliza una instrucción UPDATE para cada fila modificada.</p></td>
</tr>
</tbody>
</table>

