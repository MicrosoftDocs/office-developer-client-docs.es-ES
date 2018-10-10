---
title: ConnectModeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b39fc42259a1906891b82bf9b9ef252997e6240
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486228"
---
# <a name="connectmodeenum"></a>ConnectModeEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica los permisos disponibles para modificar datos en un objeto [Connection](connection-object-ado.md), abrir un [Record](record-object-ado.md) o especificar los valores de la propiedad [Mode](mode-property-ado.md) de los objetos **Record** y [Stream](stream-object-ado.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>1</p></td>
<td><p>Indica permisos de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3</p></td>
<td><p>Indica permisos de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0 x 400000</p></td>
<td><p>Se usa junto con los otros valores de <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>o <strong>adModeShareDenyRead</strong>) para propagar restricciones de uso compartidas a todos los registros secundarios del actual <strong>registro</strong>. No tiene ningún efecto si el <strong>registro</strong> no tiene todos los elementos secundarios. Se genera un error en tiempo de ejecución si se utiliza sólo con <strong>adModeShareDenyNone</strong> . Sin embargo, se puede usar con <strong>adModeShareDenyNone</strong> cuando se combina con otros valores. Por ejemplo, puede usar &quot; <strong>adModeUnknown</strong> o <strong>adModeShareDenyNone</strong> o <strong>adModeRecursive</strong>&quot;.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16</p></td>
<td><p>Permite a otros usuarios abrir una conexión con cualquier permiso. No se les puede denegar el acceso de lectura ni el de escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>4</p></td>
<td><p>Impide a otros usuarios abrir una conexión con permisos de lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8</p></td>
<td><p>Impide a otros usuarios abrir una conexión con permisos de escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>12</p></td>
<td><p>Impide a otros usuarios abrir una conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Valor predeterminado. Indica que aún no se han establecido los permisos o que no se pueden determinar.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Indica permisos de sólo escritura.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

Paquete: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.READ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(No existe el equivalente de AdoEnums.ConnectMode.RECURSIVE)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYNONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREDENYREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYWRITE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREEXCLUSIVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.WRITE</p></td>
</tr>
</tbody>
</table>

