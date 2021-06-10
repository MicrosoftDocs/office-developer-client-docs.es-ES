---
title: XactAttributeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302572"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**Se aplica a:** Access 2013, Office 2013

Especifica los atributos de transacción de un objeto [ Connection](connection-object-ado.md).

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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>Realiza las anulaciones de retención; es decir, al llamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">a RollbackTrans</a> se inicia automáticamente una nueva transacción. No todos los proveedores admiten esto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>Realiza confirmaciones de retención; es decir, al llamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">a CommitTrans</a> se inicia automáticamente una nueva transacción. No todos los proveedores admiten esto.</p></td>
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
<td><p>AdoEnums.XactAttribute.ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.XactAttribute.COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

