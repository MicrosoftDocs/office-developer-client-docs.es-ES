---
title: AbrirVista (acción de macro)
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699012"
---
# <a name="openview-macro-action"></a>AbrirVista (acción de macro)

**Se aplica a**: Access 2013, Office 2013

En un proyecto de Access, puede utilizar la acción **AbrirVista** para abrir una vista en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta la vista especificada cuando se abre en la vista Hoja de datos. Puede seleccionar un modo de entrada de datos para la vista y restringir los registros que muestra la vista.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **AbrirVista** tiene los siguientes argumentos.

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
<td><p><strong>Nombre de vista</strong></p></td>
<td><p>El nombre de la vista que se va a abrir. El cuadro <strong>Nombre de la vista</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las vistas en la base de datos actual. Este argumento es obligatorio. Si ejecuta una macro que contiene la acción <strong>AbrirVista</strong> en una base de datos de biblioteca, Microsoft Access primero busca la vista con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Vista en la que se abrirá la vista. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>Modo de entrada de datos para la vista. Sólo se aplica a las vistas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar registros nuevos, pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar registros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción es similar a hacer doble clic en una vista en el panel de navegación, o bien, a hacer clic con el botón secundario en la vista en el panel de navegación y, a continuación, hacer clic en el comando deseado.

> [!TIP]
> - Puede arrastrar una vista desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirVista** que abre la vista en la vista Hoja de datos.
> - Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una vista (esos mensajes indican que se trata de una vista y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.

Para ejecutar la acción **AbrirVista** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **OpenView** del objeto **DoCmd**.

