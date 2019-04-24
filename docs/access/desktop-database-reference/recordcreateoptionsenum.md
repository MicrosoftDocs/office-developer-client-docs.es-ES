---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300696"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Se aplica a:** Access 2013, Office 2013

Especifica si se debe abrir un **Record** existente o crear un **Record** nuevo para el método [Open](record-object-ado.md) del objeto [Record](open-method-ado-record.md). Los valores se pueden combinar con un operador AND.

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Crea un <strong>Record</strong> nuevo en el nodo especificado por parámetro <em>Source</em> en lugar de abrir un <strong>Record</strong> existente. Si el origen apunta a un nodo existente, se produce un error de tiempo de ejecución, a menos que <strong>adCreateCollection</strong> se combine con <strong>adOpenIfExists</strong> o <strong>adCreateOverwrite</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>comprendi</p></td>
<td><p>Crea un <strong>Record</strong> nuevo de tipo <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Modifica las marcas de creación <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> y <strong>adCreateStructDoc</strong>. Cuando se usa el operador OR con este valor y uno de los valores de marca de creación, si la dirección URL de origen apunta a un nodo o <strong>Record</strong> existente, entonces el <strong>Record</strong> se sobrescribe y se crea uno nuevo en su lugar. Este valor no se puede usar junto con <strong>adOpenIfExists</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Crea un <strong>Record</strong> nuevo de tipo <a href="recordtypeenum.md">adStructDoc</a>, en lugar de abrir un <strong>Record</strong> existente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Produce un error de tiempo de ejecución si <em>Source</em> apunta a un nodo inexistente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Modifica las marcas de creación <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> y <strong>adCreateStructDoc</strong>. Cuando se usa el operador OR con este valor y uno de los valores de marca de creación, si la dirección URL de origen apunta a un nodo o un objeto <strong>Record</strong> existente, entonces el proveedor debe abrir el <strong>Record</strong> existente en lugar de crear uno nuevo. Este valor no se puede usar junto con <strong>adCreateOverwrite</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

