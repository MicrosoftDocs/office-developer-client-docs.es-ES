---
title: CursorLocationEnum (referencia de base de datos de escritorio de Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295215"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Se aplica a:** Access 2013, Office 2013

Especifica la ubicación del servicio de cursores.

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
<td><p><strong>adUseClient</strong></p></td>
<td><p>3 </p></td>
<td><p>Usa cursores de cliente proporcionados por una biblioteca de cursores local. Los servicios de cursores locales suelen ofrecer muchas características que los cursores suministrados por controlador no facilitan, así que el uso de esta opción puede proporcionar una ventaja con respecto a las características que habilitará. Para mantener la compatibilidad con versiones anteriores, también se admite el sinónimo <strong>adUseClientBatch</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1 </p></td>
<td><p>No utiliza servicios de cursor (esta constante está obsoleta y aparece sólo para mantener la compatibilidad con versiones anteriores).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2 </p></td>
<td><p>Éste es el valor predeterminado. Usa cursores suministrados por controlador o por proveedor de datos. Estos cursores a veces son muy flexibles y permiten una sensibilidad adicional a los cambios realizados por otros en el origen de datos. Sin embargo, algunas características del Servicio de <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">cursores</a> de Microsoft para OLE DB (como objetos <a href="recordset-object-ado.md">Recordset</a> desasociados) no se pueden simular con cursores de servidor y estas características no estarán disponibles con esta configuración.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente de ADO/WFC

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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

