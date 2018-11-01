---
title: EstablecerAdvertencias (acción de macro)
TOCTitle: SetWarnings Macro Action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1a1081ac8778c143270e4e2536c53bb47982af92
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885517"
---
# <a name="setwarnings-macro-action"></a>EstablecerAdvertencias (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **EstablecerAdvertencias** para activar y desactivar los mensajes del sistema.


> [!NOTE]
> <P>[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</P>



## <a name="setting"></a>Configuración

La acción **EstablecerAdvertencias** utiliza el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Activar advertencias</strong></p></td>
<td><p>Especifica si se deben mostrar los mensajes del sistema. Haga clic en <strong>Sí</strong> (para activar los mensajes del sistema) o en <strong>No</strong> (para desactivar los mensajes del sistema) en el cuadro <strong>Activar advertencias</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>No</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar esta acción para evitar que los cuadros de mensajes y advertencias modales detengan la macro. No obstante, los mensajes de error siempre se muestran. Además, Microsoft Access muestra también los cuadros de diálogo que requieren alguna entrada que no sea simplemente elegir un botón (como **Aceptar**, **Cancelar**, **Sí** o **No**); por ejemplo, cualquier cuadro de diálogo que requiera que se escriba texto o se seleccione una de varias opciones.

Ejecutar esta acción con el argumento **Activar advertencias** establecido en **No** equivale a presionar ENTRAR cuando aparece un cuadro de mensaje o advertencia. Normalmente, se elige un botón **Aceptar** o **Sí** en respuesta al mensaje o advertencia.

Cuando termina la macro, Access vuelve a activar automáticamente la presentación de mensajes del sistema.

Esta acción se suele utilizar con la acción **Eco**, la cual permite ocultar los resultados de una macro mientras ésta se ejecuta. Puede usar entonces la acción **EstablecerAdvertencias** para ocultar también los cuadros de mensajes y advertencias.


> [!WARNING]
> <P>[!PRECAUCIóN] Aunque la acción <STRONG>EstablecerAdvertencias</STRONG> puede simplificar las interacciones con las macros, se debe tener cuidado con la desactivación de los mensajes del sistema. En algunas situaciones, no deseará continuar con una macro si aparece un determinado mensaje. A menos que esté muy seguro del resultado de todas las acciones de la macro, debería evitar utilizar esta acción.</P>



Para ejecutar la acción **EstablecerAdvertencias** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SetWarnings** del objeto **DoCmd**.

