---
title: Propiedad Recordset2.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5ffe9c679da3f11666799caa070f51f384729cc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307465"
---
# <a name="recordset2bof-property-dao"></a>Propiedad Recordset2.BOF (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve un valor que indica si la posición del registro actual está delante del primer registro en un objeto **Recordset**. **Booleano** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . BOF

*expresión* Variable que representa un objeto **Recordset2.**

## <a name="remarks"></a>Comentarios

Puede usar las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se desplazó más allá de los límites de un objeto **Recordset** cuando se mueve de un registro a otro.

La ubicación del puntero de registro actual determina los valores **BOF** y **EOF** devueltos.

Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro actual.

Si abre un objeto **Recordset** sin registros, las propiedades **BOF** y **EOF** se establecen en **True**, y el valor de la propiedad **RecordCount** del objeto **Recordset** será 0. Si abre un objeto **Recordset** con al menos un registro, el primer registro será el registro actual y las propiedades **BOF** y **EOF** serán **False**; éstas permanecerán **False** hasta que se desplace más allá del principio o del final del objeto **Recordset** mediante el método **MovePrevious** o **MoveNext**, respectivamente. Cuando se desplace más allá del principio o del final del conjunto de registros, no habrá registro actual o no existirá ningún registro.

Si elimina el último registro que queda en el objeto **Recordset**, puede que el valor de las propiedades **BOF** y **EOF** siga siendo **False** hasta que intente ajustar la posición del registro actual.

Si usa el método **MoveLast** en un objeto **Recordset** que contiene registros, el último registro será el registro actual; si, a continuación, usa el método **MoveNext**, el registro actual no será válido y la propiedad **EOF** se establecerá en **True**. A la inversa, si usa el método **MoveFirst** en un objeto **Recordset** que contiene registros, el primer registró será el registro actual; si, a continuación, usa el método **MovePrevious**, no habrá registro actual y la propiedad **BOF** se establecerá en **True**.

Generalmente cuando trabaje con todos los registros en un objeto **Recordset**, su código recorrerá los registros usando el método **MoveNext** hasta que la propiedad **EOF** se establezca en **True**.

Si utiliza el método **MoveNext** mientras la propiedad **EOF** se establece en **True**, o utiliza el método **MovePrevious** mientras la propiedad **BOF** se establece en **True**, se producirá un error.

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
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Move &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Move &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF=True,</strong><br />
<strong>EOF=False</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Permitido</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF=False,</strong><br />
<strong>EOF=True</strong></p></td>
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

Un método **OpenRecordset** llama internamente a un método **MoveFirst**. Por tanto, al utilizar un método **OpenRecordset** en un conjunto de registros vacío, se establecen las propiedades **BOF** y **EOF** en **True**. (En la siguiente tabla puede ver el comportamiento de un método **MoveFirst** cuando se produce un error).

Todos los métodos Move que se ubican en un registro con éxito, establecerán **BOF** y **EOF** en **False**.

En un área de trabajo de Microsoft Access, si agrega un registro a un conjunto de registros vacío, **BOF** será **False**, pero **EOF** permanecerá establecido en **True**, lo que indica que la posición actual se encuentra al final del conjunto de registros.

Cualquier método **Delete**, incluso si ese método quita el único registro de un conjunto de registros, no cambiará el valor de la propiedad **BOF** o **EOF**.

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
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Sin cambios</p></td>
<td><p>Sin cambios</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Sin cambios</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Sin cambios</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

