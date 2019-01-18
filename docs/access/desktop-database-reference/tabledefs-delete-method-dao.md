---
title: TableDefs.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709323"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Elimina el objeto **TableDef** especificado de la colección **TableDefs**.

## <a name="syntax"></a>Sintaxis

*expresión* . Delete (***nombre***)

*expresión* Variable que representa un objeto **TableDefs** .

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
<td><p>Nombre de TableDef que se debe eliminar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El método Delete está admitido sólo cuando el objeto **TableDef** es nuevo y no se ha anexado a la base de datos, o cuando la propiedad **Updatable** de **TableDef** está establecida en **True**.

