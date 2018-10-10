---
title: Propiedades BOF y EOF (ADO)
TOCTitle: BOF, EOF Properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 14cd61f6bd2985d71321d848a6426c06c4c7a94d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484044"
---
# <a name="bof-eof-properties-ado"></a>Propiedades BOF y EOF (ADO)


**Se aplica a**: Access 2013 | Office 2013

  - **BOF**: indica que la posición de registro actual se sitúa delante del primer registro de un objeto [Recordset](recordset-object-ado.md).

  - **EOF**: indica que la posición de registro actual se sitúa después del último registro de un objeto **Recordset**.

## <a name="return-value"></a>Valor devuelto

Las propiedades **BOF** y **EOF** devuelven valores **booleanos**.

## <a name="remarks"></a>Comentarios

Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se ha desplazado más allá de los límites de un objeto **Recordset** cuando se mueve de un registro a otro.

La propiedad **BOF** devuelve **True** (-1) si la posición de registro actual se sitúa delante del primer registro y devuelve **False** (0) si la posición de registro actual se sitúa en el primer registro o después del mismo.

La propiedad **EOF** devuelve **True** si la posición de registro actual se sitúa después del último registro y devuelve **False** si la posición de registro actual se sitúa en el último registro o delante del mismo.

Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro actual.

Si se abre un objeto **Recordset** que no contiene registros, las propiedades **BOF** y **EOF** tienen el valor **True** (vea la propiedad [RecordCount](recordcount-property-ado.md) para obtener más información sobre este estado de un objeto **Recordset**). Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el registro actual y las propiedades **BOF** y **EOF** tienen el valor **False**.

Si se elimina el último registro que queda en el objeto **Recordset**, puede que el valor de las propiedades **BOF** y **EOF** siga siendo **False** hasta que se intente ajustar la posición del registro actual.

En esta tabla se muestran los métodos **Move** permitidos con diferentes combinaciones de las propiedades **BOF** y **EOF**.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>Métodos MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Mover &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Mover &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True,</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Permitido</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False,</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="odd">
<td><p>Ambas propiedades son <strong>True</strong></p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="even">
<td><p>Ambas propiedades son <strong>False</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
</tr>
</tbody>
</table>


Si un método **Move** está permitido, esto no garantiza que busque correctamente un registro; sólo significa que las llamadas al método **Move** especificado no generarán un error.

En la tabla siguiente se muestra lo que les sucede a los valores de configuración de **BOF** y **EOF** cuando se llama a varios métodos **Move** y no se puede encontrar un registro.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p>Establecer en <strong>True</strong></p></td>
<td><p>Establecer en <strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>No cambia</p></td>
<td><p>No cambia</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>mueva</strong> &lt; 0</p></td>
<td><p>Se establece en <strong>True</strong></p></td>
<td><p>No cambia</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>mueva</strong> &gt; 0</p></td>
<td><p>No cambia</p></td>
<td><p>Se establece en <strong>True</strong></p></td>
</tr>
</tbody>
</table>

