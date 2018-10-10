---
title: Parameter.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1efe394193b9f8e74c02ecb71758d94fac9259a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483924"
---
# <a name="parametertype-property-dao"></a>Parameter.Type Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece un valor que indica el tipo operativo o de datos de un objeto. **Integer** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Tipo de

*expresión* Variable que representa un objeto **Parameter** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **[Parameter](parameter-object-dao.md)** en un área de trabajo de Microsoft Access la propiedad es de solo lectura.

Para un objeto **Parameter**, los valores o valores enteros posibles se describen en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbBigInt</strong></p></td>
<td><p>Entero grande</p></td>
</tr>
<tr class="even">
<td><p><strong>dbBinary</strong></p></td>
<td><p>Binario</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbBoolean</strong></p></td>
<td><p>Booleano</p></td>
</tr>
<tr class="even">
<td><p><strong>dbByte</strong></p></td>
<td><p>Byte</p></td>
</tr>
<tr class="odd">
<td><p><strong>CarDb</strong></p></td>
<td><p>Carácter</p></td>
</tr>
<tr class="even">
<td><p><strong>dbCurrency</strong></p></td>
<td><p>Moneda</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDate</strong></p></td>
<td><p>Fecha y hora</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecimal</strong></p></td>
<td><p>Decimal</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDouble</strong></p></td>
<td><p>Doble</p></td>
</tr>
<tr class="even">
<td><p><strong>dbFloat</strong></p></td>
<td><p>Flotante</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbGUID</strong></p></td>
<td><p>GUID</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLong</strong></p></td>
<td><p>Long</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>Binario largo (objeto OLE)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMemo</strong></p></td>
<td><p>Memo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbNumeric</strong></p></td>
<td><p>Numérico</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSingle</strong></p></td>
<td><p>Single</p></td>
</tr>
<tr class="even">
<td><p><strong>dbText</strong></p></td>
<td><p>Texto</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbTime</strong></p></td>
<td><p>Time</p></td>
</tr>
<tr class="even">
<td><p><strong>dbTimeStamp</strong></p></td>
<td><p>Marca de hora</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVarBinary</strong></p></td>
<td><p>VarBinary</p></td>
</tr>
</tbody>
</table>


Cuando anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el nuevo objeto.

