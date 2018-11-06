---
title: Indexes.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c725919b6509b5c802502fc8280823c407516f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998829"
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
<td><p><strong>String</strong></p></td>
<td><p>Nombre del índice que se va a eliminar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El método **Delete** sólo se admite cuando el objeto **Index** es nuevo y no se ha anexado a la base de datos.

