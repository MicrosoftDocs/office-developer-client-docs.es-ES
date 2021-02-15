---
title: EstablecerCampo (acción de macro)
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314619"
---
# <a name="setfield-macro-action"></a>EstablecerCampo (acción de macro)

**Se aplica a:** Access 2013, Office 2013

La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo.

> [!NOTE]
> La acción **EstablecerCampo** solo está disponible en macros de datos.

## <a name="setting"></a>Setting

La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Una cadena que identifica el campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Valor</strong></p></td>
<td><p>Expresión que especifica el valor que se asignará al campo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

No se puede utilizar la acción **EstablecerCampo** fuera de un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)**.

