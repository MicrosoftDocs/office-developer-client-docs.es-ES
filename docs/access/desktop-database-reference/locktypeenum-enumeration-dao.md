---
title: Enumeración LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289860"
---
# <a name="locktypeenum-enumeration-dao"></a>Enumeración LockTypeEnum (DAO)


**Se aplica a:** Access 2013, Office 2013

Especifica el tipo de bloqueo de registros que se utiliza al abrir un conjunto de registros.

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
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>Concurrencia optimista basada en el identificador de registro. El cursor compara el identificador de registro en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Habilita actualizaciones optimistas por lotes (áreas de trabajo de ODBCDirect únicamente).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Concurrencia optimista basada en los valores de registro. El cursor compara los valores de datos en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez (áreas de trabajo de ODBCDirect únicamente).</p>

> [!NOTE]
> Las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Utilice ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Concurrencia pesimista. El cursor utiliza el nivel de bloqueo más bajo suficiente para garantizar que el registro se puede actualizar.</p></td>
</tr>
</tbody>
</table>

