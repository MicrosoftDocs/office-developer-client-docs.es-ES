---
title: CursorLocationEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484695"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica la ubicación del servicio de cursores.

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
<td><p>3</p></td>
<td><p>Utiliza cursores de cliente suministrados por una biblioteca de cursores local. Servicios de cursores locales a menudo le permitirá muchas características que los cursores suministrados por controlador no podrán, por lo que el uso de esta configuración puede proporcionar una ventaja con respecto a las características que se habilitará. Para compatibilidad con versiones anteriores, también se admite el sinónimo <strong>adUseClientBatch</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>No utiliza servicios de cursor (esta constante está obsoleta y aparece sólo para mantener la compatibilidad con versiones anteriores).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Valor predeterminado. Usa cursores suministrados por controlador o por proveedor de datos. Estos cursores a veces son muy flexibles y permiten una sensibilidad adicional a los cambios realizados por otros en el origen de datos. No obstante, algunas características del <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Servicio de cursores de Microsoft para OLE DB</a> (como los objetos <a href="recordset-object-ado.md">Recordset</a> desasociados) no se pueden simular con cursores de servidor y dichas características no estarán disponibles con esta opción.</p></td>
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

