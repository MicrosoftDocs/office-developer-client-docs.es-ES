---
title: Resumen del modelo de objetos de RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300878"
---
# <a name="rds-object-model-summary"></a>Resumen del modelo de objetos de RDS


**Se aplica a:** Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS. DataSpace</a></p></td>
<td><p>Este objeto contiene un método para obtener un proxy de servidor. El proxy puede ser el programa de servidor predeterminado o un programa de servidor personalizado (objeto de negocio). El programa de servidor puede invocarse en Internet, una intranet, una red de área local, o puede ser una biblioteca de vínculos dinámicos local.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></p></td>
<td><p>Este objeto representa el programa de servidor predeterminado.

Ejecuta el comportamiento predeterminado de recuperación y actualización de datos de RDS.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS. DataControl</a></p></td>
<td><p>Este objeto puede invocar automáticamente los objetos <strong>RDS.DataSpace</strong> y <strong>RDSServer.DataFactory</strong>. Utilice este objeto para invocar el comportamiento predeterminado de recuperación y actualización de datos de RDS. Este objeto también permite a los controles visuales obtener acceso al objeto <strong>Recordset</strong> devuelto.</p></td>
</tr>
</tbody>
</table>

