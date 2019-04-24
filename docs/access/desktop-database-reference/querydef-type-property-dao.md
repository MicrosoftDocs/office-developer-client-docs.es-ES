---
title: Propiedad QueryDef. Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300948"
---
# <a name="querydeftype-property-dao"></a>Propiedad QueryDef. Type (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. InTeger de**** sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Type

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Comentarios

Para un objeto **QueryDef**, los valores o valores enteros posibles se muestran en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Tipo de consulta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbQAction</strong></p></td>
<td><p>Acción</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQAppend</strong></p></td>
<td><p>Anexar</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQCompound</strong></p></td>
<td><p>Compuestos</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Referencias cruzadas</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Definición de datos</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Eliminar</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Creación de tabla</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Procedimiento (sólo áreas de trabajo de ODBCDirect)</p><p><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Select</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSPTBulk</strong></p></td>
<td><p>Utilizada con <strong>dbQSQLPassThrough</strong> para especificar una consulta que no devuelve registros (sólo para áreas de trabajo de Microsoft Access)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSQLPassThrough</strong></p></td>
<td><p>Paso a través (sólo para áreas de trabajo de Microsoft Access)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


Cuando se anexa un nuevo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** o **[Property](property-object-dao.md)** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.

