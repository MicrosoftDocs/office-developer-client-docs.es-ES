---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc3803fe6afb482dc42ca12476024325fc1022ae
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862985"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica la dirección de una búsqueda de registro dentro de un objeto [Recordset](recordset-object-ado.md).

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
<td><p><strong>adSearchBackward</strong></p></td>
<td><p>-1</p></td>
<td><p>Busca hacia atrás y se detiene al principio del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md">BOF</a> (inicio del archivo).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSearchForward</strong></p></td>
<td><p>1</p></td>
<td><p>Busca hacia adelante y se detiene al final del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md"> EOF</a> (fin del archivo).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

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
<td><p>AdoEnums.SearchDirection.BACKWARD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.SearchDirection.FORWARD</p></td>
</tr>
</tbody>
</table>

