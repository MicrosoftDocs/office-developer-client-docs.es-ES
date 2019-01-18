---
title: Indexes.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703548"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Elimina el objeto **Index** especificado de la colección **Indexes**.

## <a name="syntax"></a>Sintaxis

*expresión* . Delete (***nombre***)

*expresión* Variable que representa un objeto **Indexes** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Nombre del índice que se va a eliminar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El método **Delete** sólo se admite cuando el objeto **Index** es nuevo y no se ha anexado a la base de datos.

