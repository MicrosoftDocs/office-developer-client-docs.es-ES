---
title: Método CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295341"
---
# <a name="createrecordset-method-rds"></a>Método CreateRecordset (RDS)

**Se aplica a:** Access 2013, Office 2013

Crea un objeto [Recordset](recordset-object-ado.md) vacío y desconectado.

## <a name="syntax"></a>Sintaxis

*objeto*. CreateRecordset (*ColumnInfos*)

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Object* |Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) o [RDS.DataControl](datacontrol-object-rds.md).|
|*ColumnsInfos* |Matriz de atributos **Variant** que define cada columna del objeto **Recordset** creado. Cada definición de columna contiene una matriz de cuatro atributos necesarios y un atributo opcional. A continuación, el conjunto de matrices de columnas se agrupa en una matriz, que define el **Recordset**. Para obtener una lista de atributos, vea la tabla siguiente.|

### <a name="variant-array-attributes"></a>Atributos de matriz Variant

|Atributo|Descripción|
|:--------|:----------|
|Name |Nombre del encabezado de columna.|
|Tipo |Entero del tipo de datos.|
|Size |Entero del ancho en caracteres, independientemente del tipo de datos.|
|Aceptación de null |Valor booleano.|
|Scale (opcional) |Este atributo opcional define la escala de los campos numéricos.

Si no se especifica este valor, los valores numéricos se truncarán en una escala de tres.

No se ve afectada la precisión, pero el número de dígitos después del separador decimal se truncará en tres.|

## <a name="remarks"></a>Comentarios

El objeto de negocio de servidor puede rellenar el objeto **Recordset** resultante con los datos de un proveedor de datos que no sea OLE DB, como un archivo de sistema operativo que contiene cotizaciones.

En la tabla siguiente figuran los valores de [DataTypeEnum](datatypeenum.md) admitidos por el método **CreateRecordset**. El número que aparece es el número de referencia usado para definir los campos.

Cada uno de los tipos de datos es de longitud fija o longitud variable.

Los tipos de longitud fija deben definirse con un tamaño de -1, porque el tamaño viene previamente determinado y se sigue requiriendo una definición de tamaño.

Los tipos de datos de longitud variable permiten un tamaño que oscila entre 1 y 32767.

Para algunos de los tipos de datos de longitud variable, puede que el tipo se convierta en el tipo que aparece en la columna Sustitución. Las sustituciones no se verán hasta que se cree y se rellene el objeto **Recordset**. Después, se podrá buscar el tipo de datos real, si es necesario.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Length</p></th>
<th><p>Constante</p></th>
<th><p>Número</p></th>
<th><p>Sustitutivo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>segundo</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>432</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>dieciocho</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>18</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>2,5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6,5</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>apartado</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>12</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>metros</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>0,7</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Decimal</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Decimal</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>0,7</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8,5</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

