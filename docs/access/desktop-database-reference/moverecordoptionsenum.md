---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bd8196670513156011d69f08eacf790fa4a0a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288675"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Se aplica a:** Access 2013, Office 2013

Especifica el comportamiento del método [MoveRecord](record-object-ado.md) del objeto [Record](moverecord-method-ado.md).

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
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Realiza la operación mover predeterminada: la operación falla si el archivo o el directorio de destino ya existen; por otro lado, la operación actualiza los vínculos de hipertexto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Sobrescribe el archivo o el directorio de destino, incluso si ya existen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Modifica el comportamiento predeterminado del método <strong>MoveRecord</strong>, no actualizando los vínculos de hipertexto del <strong>Record</strong> de origen. El comportamiento predeterminado depende de las capacidades del proveedor. La operación mover actualiza los vínculos si el proveedor es capaz. Si el proveedor no puede reparar vínculos, o si no se especifica este valor, entonces la operación de movimiento funcionará incluso aunque los vínculos no se hayan reparado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4 </p></td>
<td><p>Solicita que el proveedor intente simular la operación de movimiento (mediante operaciones de descarga, carga y eliminación). Si el intento de mover el <strong>Record</strong> falla debido a que la dirección URL de destino está en un servidor diferente o atendida por un proveedor diferente del de origen, esto puede ocasionar un aumento de latencia o pérdida de datos debido a diferencias de capacidades de los proveedores al mover recursos entre ellos.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente a ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

