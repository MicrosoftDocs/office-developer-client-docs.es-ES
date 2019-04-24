---
title: Propiedad Recordset. Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307556"
---
# <a name="recordsettype-property-dao"></a>Propiedad Recordset. Type (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Type

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

Para un objeto **Recordset**, los valores posibles y valores devueltos son los que se muestran a continuación.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Tipo Recordset</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbOpenTable</strong></p></td>
<td><p>Tabla (sólo para áreas de trabajo de Microsoft Access)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>Dinámico (sólo áreas de trabajo de ODBCDirect)</p>
<p><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>Dinámico</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>Copias</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>Solo avance</p></td>
</tr>
</tbody>
</table>

