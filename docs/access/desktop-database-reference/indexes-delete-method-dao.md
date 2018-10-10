---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484201"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Elimina el objeto **Index** especificado de la colección **Indexes**.

## <a name="syntax"></a>Sintaxis

*expresión* . Delete (***nombre***)

*expresión* Variable que representa un objeto **Indexes** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nombre del índice que se va a eliminar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El método **Delete** sólo se admite cuando el objeto **Index** es nuevo y no se ha anexado a la base de datos.

