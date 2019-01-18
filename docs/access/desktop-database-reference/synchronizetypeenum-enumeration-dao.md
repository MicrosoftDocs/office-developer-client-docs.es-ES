---
title: SynchronizeTypeEnum (enumeración) (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acd4ca20e9b6e17f28a17b012bb182060471e949
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725885"
---
# <a name="synchronizetypeenum-enumeration-dao"></a>SynchronizeTypeEnum (enumeración) (DAO)


**Se aplica a**: Access 2013, Office 2013

Se utiliza con el método **Synchronize** para determinar el tipo de sincronización que se ha de aplicar a dos réplicas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbRepExportChanges</p></td>
<td><p>1</p></td>
<td><p>Envía cambios de la base de datos actual a la base de datos de destino.</p></td>
</tr>
<tr class="even">
<td><p>dbRepImpExpChanges</p></td>
<td><p>4</p></td>
<td><p>Envía y recibe datos en un intercambio bidireccional.</p></td>
</tr>
<tr class="odd">
<td><p>dbRepImportChanges</p></td>
<td><p>2</p></td>
<td><p>Recibe cambios de la base de datos de destino.</p></td>
</tr>
<tr class="even">
<td><p>dbRepSyncInternet</p></td>
<td><p>16</p></td>
<td><p>Envía y recibe datos en un intercambio bidireccional.</p></td>
</tr>
</tbody>
</table>

