---
title: QueryDef.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5129f4a50f056259c5b556c8e8ea408358718d3c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484619"
---
# <a name="querydeftype-property-dao"></a>QueryDef.Type Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Tipo de

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

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
<td><p>Compuesta</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Tabla de referencias cruzadas</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Definición de datos</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Delete</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Creación de tabla</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Procedimiento (sólo áreas de trabajo de ODBCDirect)</p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Selección</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Unión</p></td>
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

