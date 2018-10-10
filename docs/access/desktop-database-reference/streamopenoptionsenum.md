---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3998f41c1400a2870633f19228cbf73189e9527a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485468"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica opciones para abrir un objeto [Stream](stream-object-ado.md). Los valores se pueden combinar con una operación booleana OR (O).

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
<td><p><strong>adOpenStreamAsync</strong></p></td>
<td><p>1</p></td>
<td><p>Abre el objeto <strong>Stream</strong> en modo asincrónico.</p></td>
</tr>
<tr class="even">
<td><p><strong>OpenOptions</strong></p></td>
<td><p>4</p></td>
<td><p>Identifica el contenido del parámetro <em>Source</em> (origen) como un objeto <a href="record-object-ado.md">Record</a> ya abierto. El comportamiento predeterminado consiste en tratar <em>Source</em> como una dirección URL que señala directamente a un nodo de una estructura de árbol. Se abre la secuencia predeterminada asociada a ese nodo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Especifica que el objeto <strong>Stream</strong> se abra con opciones predeterminadas.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

Estas constantes no tienen equivalentes ADO/WFC.

