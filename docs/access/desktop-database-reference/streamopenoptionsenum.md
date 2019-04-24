---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314752"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Se aplica a:** Access 2013, Office 2013

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
<td><p><strong>Openoptions</strong></p></td>
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


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

