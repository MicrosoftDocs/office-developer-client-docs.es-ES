---
title: Método Indexes. Append (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291654"
---
# <a name="indexesappend-method-dao"></a>Método Indexes. Append (DAO)

**Se aplica a:** Access 2013, Office 2013

Agrega un nuevo objeto **Index** a la colección **Indexes**.

## <a name="syntax"></a>Sintaxis

*expresión* . Append (***objeto***)

*expresión* Variable que representa un objeto **Indexes** .

## <a name="parameters"></a>Parameters

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
<td><p><em>Object</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Objeto</strong></p></td>
<td><p>Variable de objeto que representa un elemento que se va a agregar a la colección.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.

La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.

Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error. Por ejemplo, si no ha especificado un tipo de campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef** , al usar el método **Append** se desencadena un error en tiempo de ejecución.

