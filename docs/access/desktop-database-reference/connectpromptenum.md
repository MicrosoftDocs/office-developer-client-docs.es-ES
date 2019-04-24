---
title: ConnectPromptEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295670"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**Se aplica a:** Access 2013, Office 2013

Especifica si se debe mostrar un cuadro de diálogo para solicitar los parámetros que faltan al abrir una conexión con un origen de datos.

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
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Solicita información siempre.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>segundo</p></td>
<td><p>Solicita más información si se necesita.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>Solicita más información si se necesita, pero no se admiten parámetros opcionales.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>No solicita información nunca.</p></td>
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
<td><p>AdoEnums. ConnectPrompt. ALWAYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectPrompt. COMPLETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectPrompt. COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectPrompt. NEVER</p></td>
</tr>
</tbody>
</table>

