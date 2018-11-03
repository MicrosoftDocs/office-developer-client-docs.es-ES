---
title: DataTypeEnum (enumeración) (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5c4486ab78efa386b2d5f1c2ca63f464823eb23
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947675"
---
# <a name="datatypeenum-enumeration-dao"></a>DataTypeEnum (enumeración) (DAO)


**Se aplica a**: Access 2013, Office 2013

Especifica el tipo de datos operativo de un objeto.

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
<td><p>dbAttachment</p></td>
<td><p>101</p></td>
<td><p>Datos adjuntos</p></td>
</tr>
<tr class="even">
<td><p>dbBigInt</p></td>
<td><p>16</p></td>
<td><p>Datos enteros grandes</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9</p></td>
<td><p>Datos binarios</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Datos booleanos (Verdadero/Falso)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Datos de byte (8 bits)</p></td>
</tr>
<tr class="even">
<td><p>CarDb</p></td>
<td><p>18</p></td>
<td><p>Datos de texto (ancho fijo)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Datos de byte multivalor</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Datos decimales multivalor</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Datos de punto flotante de doble precisión multivalor</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Datos GUID multivalor</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Datos enteros multivalor</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Datos enteros largos multivalor</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Datos de punto flotante de precisión simple multivalor</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Datos de texto multivalor (ancho variable)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Datos de moneda</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8</p></td>
<td><p>Datos de valores de fecha</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Datos decimales (ODBCDirect únicamente)</p><p><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
</td>
</tr>
<tr class="even">
<td><p>dbDouble</p></td>
<td><p>7</p></td>
<td><p>Datos de punto flotante de doble precisión</p></td>
</tr>
<tr class="odd">
<td><p>dbFloat</p></td>
<td><p>21</p></td>
<td><p>Datos de punto flotante (ODBCDirect únicamente)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15</p></td>
<td><p>Datos GUID</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Datos enteros</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Datos enteros largos</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Datos binarios (mapa de bits)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12</p></td>
<td><p>Datos de tipo Memo (texto extendido)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Datos numéricos (ODBCDirect únicamente)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6</p></td>
<td><p>Datos de punto flotante de precisión simple</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Datos de texto (ancho variable)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Datos en formato de hora (ODBCDirect únicamente)</p>

<br/>


</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Datos en formato de fecha y hora (ODBCDirect únicamente)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17</p></td>
<td><p>Datos binarios variables (ODBCDirect únicamente)</p>

<br/>


</td>
</tr>
</tbody>
</table>

