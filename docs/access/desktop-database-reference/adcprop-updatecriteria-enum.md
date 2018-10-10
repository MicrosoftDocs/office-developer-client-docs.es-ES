---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b018402f6a2d48819a3f97c69e2a8db77fa9e84c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486793"
---
# <a name="adcpropupdatecriteriaenum"></a>ADCPROP\_UPDATECRITERIA\_ENUM

**Se aplica a**: Access 2013 | Office 2013

Especifica qué campos se pueden usar para detectar conflictos durante una actualización optimista de una fila del origen de datos con un objeto [Recordset](recordset-object-ado.md).

Use estas constantes con la propiedad dinámica "**Update Criteria**" del objeto **Recordset**, que aparece en el [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) y se explica en la documentación del [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).

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
<td><p><strong>adCriteriaAllCols</strong></p></td>
<td><p>1</p></td>
<td><p>Detecta conflictos si se ha cambiado cualquier columna de la fila del origen de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>Detecta conflictos si se ha cambiado la columna de clave de la fila del origen de datos; es decir, se ha eliminado la fila.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3</p></td>
<td><p>Detecta conflictos si la marca de tiempo de la fila del origen de datos ha cambiado; es decir, se ha tenido acceso a la fila después de obtenerse el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2</p></td>
<td><p>Detecta conflictos si se han cambiado columnas de la fila del origen de datos correspondientes a campos actualizados del objeto <strong>Recordset</strong>.</p></td>
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
<td><p>AdoEnums.AdcPropUpdateCriteria.ALLCOLS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.KEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.UPDCOLS</p></td>
</tr>
</tbody>
</table>

