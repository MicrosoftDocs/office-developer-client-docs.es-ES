---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33347492562d868781e8bbca346918d55ed597b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860283"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica el comportamiento del método [CopyRecord](copyrecord-method-ado.md).

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
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que el proveedor <em>Origen</em> intenta simular la copia mediante operaciones de descarga y carga si este método falla debido a que <em>Destino</em> está en un servidor diferente o es atendido por un proveedor diferente de <em>Origen</em>. Tenga en cuenta que las capacidades diferentes de los proveedores pueden dificultar el rendimiento u ocasionar la pérdida de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Copia el directorio actual, pero ninguno de sus subdirectorios, en el destino. La operación de copia no es recursiva.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Sobrescribe el archivo o el directorio si el <em>Destino</em> apunta a un archivo o directorio existentes.</p></td>
</tr>
<tr class="even">
<td><p><strong>Como</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Realiza la operación de copia predeterminada: la operación falla si el archivo o el directorio de destino ya existen, y la operación copia de forma recursiva.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

