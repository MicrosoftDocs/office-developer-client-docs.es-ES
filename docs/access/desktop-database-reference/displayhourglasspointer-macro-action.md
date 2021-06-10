---
title: MostrarCursorDeRelojDeArena (acción de macro)
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293836"
---
# <a name="displayhourglasspointer-macro-action"></a>MostrarCursorDeRelojDeArena (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **MostrarCursorDeRelojDeArena** para cambiar el puntero del mouse por la imagen de un reloj de arena (u otro icono que se elija) mientras se ejecuta una macro. Esta acción puede proporcionar una indicación visual de que la macro está ejecutándose. Resulta especialmente útil cuando una acción de macro o la propia macro tarda mucho tiempo en ejecutarse.

## <a name="setting"></a>Configuración

La acción **MostrarCursorDeRelojDeArena** tiene el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Reloj de arena activo</strong></p></td>
<td><p>Haga clic en <strong>Sí</strong> (para mostrar el icono) o en <strong>No</strong> (para mostrar el puntero normal del mouse) en el cuadro <strong>Reloj de arena activo</strong> de la sección <strong>Argumentos de acción</strong> en el panel Generador de macros. El valor predeterminado es <strong>Sí</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción se suele usar si se ha desactivado el eco mediante la acción **Eco**. Cuando el eco está desactivado, Access suspende las actualizaciones de pantalla hasta que finalice la macro.

Access restablece automáticamente el argumento **Reloj de arena activo** en **No** cuando la macro deja de ejecutarse.

> [!NOTE]
> - En Microsoft Windows, es el icono que se establece para **Ocupado** en el cuadro de diálogo **Propiedades de Mouse** del Panel de control de Windows. El icono predeterminado para todos los sistemas operativos Windows es un reloj de arena animado.
> - Si lo desea, puede elegir otro icono.

Para ejecutar la acción **MostrarCursorDeRelojDeArena** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RelojDeArena** del objeto **DoCmd**.

