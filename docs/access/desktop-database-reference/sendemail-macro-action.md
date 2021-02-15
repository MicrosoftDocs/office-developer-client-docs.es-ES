---
title: EnviarCorreoElectrónico (acción de macro)
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314654"
---
# <a name="sendemail-macro-action"></a>EnviarCorreoElectrónico (acción de macro)

**Se aplica a:** Access 2013, Office 2013

La **acción EnviarEmail** envía un mensaje de correo electrónico.

> [!NOTE]
> La acción **EnviarCorreoElectrónico** solo está disponible en macros de datos.

## <a name="setting"></a>Setting

La acción **EnviarCorreoElectrónico** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Necesario</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Para</strong></p></td>
<td><p>Sí</p></td>
<td><p>Los destinatarios del mensaje cuyos nombres desea colocar en la <strong>línea Para</strong> del mensaje. Separe los nombres de destinatario que especifique en este argumento (y en los argumentos <em>CC</em> y <em>CCO)</em> con un punto y coma (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>No</p></td>
<td><p>Destinatarios del mensaje cuyos nombres desea colocar en la línea CC (copia &quot; &quot; de carbón) del mensaje.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>No</p></td>
<td><p>Destinatarios del mensaje cuyos nombres desea colocar en la línea CCO (copia &quot; &quot; oculta) del mensaje.</p></td>
</tr>
<tr class="even">
<td><p><strong>Asunto</strong></p></td>
<td><p>No</p></td>
<td><p>Asunto del mensaje. Este texto aparece en la línea <strong>Asunto</strong> del mensaje.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cuerpo</strong></p></td>
<td><p>No</p></td>
<td><p>El texto que desea incluir en el cuerpo principal del mensaje de correo. Si deja en blanco este argumento, no se incluirá ningún texto adicional en el mensaje.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **EnviarCorreoElectrónico** solo está disponible en los eventos de macro **[Después de eliminar](after-delete-macro-event.md)**, **[Después de insertar](after-insert-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.

La acción **EnviarCorreoElectrónico** no muestra el mensaje para su edición.

