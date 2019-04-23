---
title: ObjectStateEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288528"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**Se aplica a:** Access 2013, Office 2013

Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.

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
<td><p><strong>adStateClosed</strong></p></td>
<td><p>comprendi</p></td>
<td><p>Indica que el objeto está cerrado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateOpen</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que el objeto está abierto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateConnecting</strong></p></td>
<td><p>segundo</p></td>
<td><p>Indica que el objeto se está conectando.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateExecuting</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que el objeto está ejecutando un comando.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateFetching</strong></p></td>
<td><p>8,5</p></td>
<td><p>Indica que se están recuperando las filas del objeto.</p></td>
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
<td><p>AdoEnums. state. CLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. state. OPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. state. CONNECTing</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. state. EXECUTing</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. state. FETCH</p></td>
</tr>
</tbody>
</table>

