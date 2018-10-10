---
title: ConnectOptionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483670"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica si el método [Open](open-method-ado-connection.md) de un objeto [Connection](connection-object-ado.md) debe volver después (sincrónicamente) o antes (asincrónicamente) de que la conexión se establezca.

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
<td><p><strong>adAsyncConnect</strong></p></td>
<td><p>16</p></td>
<td><p>Abre la conexión asincrónicamente. El evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> se puede utilizar para determinar en qué momento está disponible la conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong>adConnectUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Abre la conexión sincrónicamente.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

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
<td><p>AdoEnums.ConnectOption.ASYNCCONNECT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectOption.CONNECTUNSPECIFIED</p></td>
</tr>
</tbody>
</table>

