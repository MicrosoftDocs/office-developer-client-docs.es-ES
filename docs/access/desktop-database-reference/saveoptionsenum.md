---
title: SaveOptionsEnum (referencia de base de datos de escritorio de Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314745"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**Se aplica a:** Access 2013, Office 2013

Especifica si un archivo se debe crear o sobrescribir al guardar desde un objeto [Stream](stream-object-ado.md). Los valores se pueden combinar con un operador AND (Y).

<br/>

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
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1 </p></td>
<td><p>Valor predeterminado. Crea un archivo nuevo si el archivo especificado por el parámetro <em>FileName</em> aún no existe.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSaveCreateOverWrite</strong></p></td>
<td><p>2 </p></td>
<td><p>Si el archivo especificado por el parámetro <em>FileName</em> ya existe, se sobrescribe el archivo con los datos del objeto <strong>Stream</strong> actualmente abierto.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente a ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

