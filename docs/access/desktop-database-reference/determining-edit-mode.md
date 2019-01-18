---
title: Determinar el modo de edición
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698753"
---
# <a name="determining-edit-mode"></a>Determinar el modo de edición


**Se aplica a**: Access 2013, Office 2013

ADO mantiene un búfer de edición asociado al registro activo. La propiedad **EditMode** indica si se han realizado cambios en él o si se han creado registros nuevos. Utilice **EditMode** para determinar el estado de edición del registro activo. Puede comprobar si hay cambios pendientes si se ha interrumpido un proceso de edición y determinar si se necesita utilizar los métodos **Update** o **CancelUpdate**.

**EditMode** devuelve una de las constantes **EditModeEnum** incluidas en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>Indica que no se está realizando ninguna operación de edición.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Indica que los datos del registro actual se han modificado, pero no se han guardado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Indica que se ha llamado al método <strong>AddNew</strong> y que el registro activo en el búfer de copia es un nuevo registro que no se ha guardado en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Indica que se ha eliminado el registro actual.</p></td>
</tr>
</tbody>
</table>


**EditMode** sólo puede devolver un valor válido si hay un registro activo. **EditMode** devolverá un error si **BOF** o **EOF** son **True** o si se ha eliminado el registro activo.

