---
title: UpdateTypeEnum (enumeración) (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d38cf4554837c9c6434b7607746f2c40836ac950
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944623"
---
# <a name="updatetypeenum-enumeration-dao"></a>UpdateTypeEnum (enumeración) (DAO)


**Se aplica a**: Access 2013, Office 2013

Se utiliza con el método **Update** para especificar qué actualizaciones se han de escribir en el disco.

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
<td><p>dbUpdateBatch</p></td>
<td><p>4</p></td>
<td><p>Todos los cambios pendientes de la caché de actualizaciones se escriben en el disco.</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>Sólo los cambios pendientes del registro actual se escriben en el disco.</p></td>
</tr>
<tr class="odd">
<td><p>valores dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(Valor predeterminado) Los cambios pendientes no se almacenan en caché y se escriben en el disco inmediatamente.</p></td>
</tr>
</tbody>
</table>

