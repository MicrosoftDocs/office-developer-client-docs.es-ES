---
title: Propiedad Recordset.EOF (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 931de7dfc2cfb80726aafe7077c6107ec65d2f40
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719494"
---
# <a name="recordseteof-property-dao"></a>Propiedad Recordset.EOF (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica si la posición actual del registro se encuentra después del último registro en un objeto **Recordset**. **Boolean** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . EOF

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Puede usar las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se desplazó más allá de los límites de un objeto **Recordset** cuando se mueve de un registro a otro.

La ubicación del puntero de registro actual determina los valores **BOF** y **EOF** devueltos.

Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro actual.

Si abre un objeto **Recordset** sin registros, las propiedades **BOF** y **EOF** se configuran en **True**, y el valor de la propiedad **RecordCount** del objeto **Recordset** será 0. Si abre un objeto **Recordset** con al menos un registro, el primer registro será el registro actual, y las propiedades **BOF** y **EOF** serán **False**; estas serán **False** hasta que se desplace más allá del principio o del final del objeto **Recordset** mediante el método **MovePrevious** o **MoveNext**, respectivamente. Cuando se desplace más allá del principio o del final del **Recordset**, no habrá registro actual o no existirá ningún registro.

Si elimina el último registro que queda en el objeto **Recordset**, puede que el valor de las propiedades **BOF** y **EOF** siga siendo **False** hasta que intente ajustar la posición del registro actual.

Si usa el método **MoveLast** en un objeto **Recordset** que contiene registros, el último registro será el registro actual; si usa el método **MoveNext**, el registro actual no será válido y la propiedad **EOF** se configurará en **True**. A la inversa, si usa el método **MoveFirst** en un objeto **Recordset** que contiene registros, el primer registró será el registro actual; si usa el método **MovePrevious**, no habrá registro actual y la propiedad **BOF** se configurará en **True**.

Generalmente al trabajar con todos los registros en un objeto **Recordset**, el código repetirá los registros con el método **MoveNext** hasta que la propiedad **EOF** se configure en **True**.

Si usa el método **MoveNext** mientras la propiedad **EOF** se configura en **True**, o usa el método **MovePrevious** mientras la propiedad **BOF** se configura en **True**, se producirá un error.

En esta tabla se muestran los métodos Move permitidos con diferentes combinaciones de las propiedades **BOF** y **EOF**.

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


Permitir un método Move no significa que ese método se ubique correctamente en un registro. Simplemente indica que se permite un intento para realizar el método Move especificado y que no se producirá un error. El estado de las propiedades **BOF** y **EOF** puede cambiar como resultado del intento de Move.

Un método **OpenRecordset** invoca internamente a un método **MoveFirst**. Por tanto, usar un método **OpenRecordset** en un conjunto de registros vacío, configura las propiedades **BOF** y **EOF** en **True**. (En la siguiente tabla puede ver el comportamiento de un método **MoveFirst** cuando se produce un error).

Todos los métodos Move que se ubican correctamente en un registro, configurarán **BOF** y **EOF** en **False**.

En un área de trabajo de Microsoft Access, si agrega un registro a un **Recordset** vacío, **BOF** será **False**, pero **EOF** seguirá en **True**, lo que indica que la posición actual se encuentra al final del **Recordset**.

Cualquier método **Delete**, incluso si quita el único registro de un **Recordset**, no cambiará la configuración de la propiedad **BOF** o **EOF**.

En la siguiente tabla se muestra cómo los métodos Move que no han ubicado un registro afectan a la configuración de las propiedades **BOF** y **EOF**.

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
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>No cambia</p></td>
<td><p>No cambia</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>mueva</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>No cambia</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>mueva</strong> &gt; 0</p></td>
<td><p>No cambia</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

