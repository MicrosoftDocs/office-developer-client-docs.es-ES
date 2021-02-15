---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280525"
---
# <a name="adcprop_autorecalc_enum"></a>ADCPROP \_ AUTORECALC \_ ENUM

**Se aplica a:** Access 2013, Office 2013

Especifica cuándo el proveedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) debe volver a calcular las columnas agregadas y calculadas de un objeto Recordset jerárquico.

Estas constantes solo se usan con el proveedor **MSDataShape** y la propiedad dinámica **Recordset** "**Auto Recalc**", a la que se hace referencia en el índice de propiedades dinámicas de [ADO](ado-dynamic-property-index.md) y se documenta en el Servicio de [cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) de Microsoft para OLE DB o el Servicio de forma de datos de Microsoft para la documentación [de OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1 </p></td>
<td><p>Valor predeterminado. Vuelve a calcular siempre que el proveedor <strong>MSDataShape</strong> determine que han cambiado los valores de los que dependen las columnas calculadas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Calcula solo al generar inicialmente el objeto <strong>Recordset</strong> jerárquico.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente de ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

