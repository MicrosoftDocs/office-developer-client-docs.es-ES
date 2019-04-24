---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295488"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Se aplica a:** Access 2013, Office 2013

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
<td><p>segundo</p></td>
<td><p>Copia el directorio actual, pero ninguno de sus subdirectorios, en el destino. La operación de copia no es recursiva.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Sobrescribe el archivo o el directorio si el <em>Destino</em> apunta a un archivo o directorio existentes.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Realiza la operación de copia predeterminada: la operación falla si el archivo o el directorio de destino ya existen, y la operación copia de forma recursiva.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

