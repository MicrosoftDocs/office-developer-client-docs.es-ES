---
title: RegistrarEvento (acción de macro)
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 093313028822bebea26fbf86dfc94063e5512e14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873379"
---
# <a name="logevent-macro-action"></a>RegistrarEvento (acción de macro)


**Se aplica a**: Access 2013, Office 2013

La acción **RegistrarEvento** escribe información en la tabla de sistema **USysApplicationLog**.


> [!NOTE]
> <P>[!NOTA] La acción <STRONG>RegistrarEvento</STRONG> solo está disponible en macros de datos.</P>



## <a name="setting"></a>Valores

La acción **RegistrarEvento** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Descripción</strong></p></td>
<td><p>No</p></td>
<td><p>Una expresión de cadena que describe la condición que desea registrar. La descripción no puede superar los 255 caracteres.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **RegistrarEvento** puede utilizarse para escribir información de estado en la tabla de sistema **USysApplicationLog** que no puede utilizar la acción **[ProvocarError](raiseerror-macro-action.md)** para provocar un error. Por ejemplo, puede registrar los cambios realizados en un campo específico o usar los elementos que se escriben en la tabla **USysApplicationLog** para ayudarle a depurar la macro.

Si utiliza la acción **RegistrarEvento** para escribir en la tabla **USysApplicationLog**, la columna **Categoría** se establece automáticamente en **Usuario**.

Para ver la tabla **USysApplicationLog**, siga estos pasos:

1.  Haga clic en el menú **Archivo** y, a continuación, haga clic en **Opciones**.

2.  En el cuadro de diálogo **Opciones de Access**, haga clic en la pestaña **Base de datos actual**.

3.  En la sección **Navegación**, haga clic en **Opciones de navegación**.

4.  En el cuadro de diálogo **Opciones de navegación**, haga clic en **Mostrar objetos del sistema** y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **Aceptar** para descartar el cuadro de diálogo **Opciones de Access**.

