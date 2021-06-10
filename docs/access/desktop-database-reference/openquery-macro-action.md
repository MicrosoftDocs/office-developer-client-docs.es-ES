---
title: AbrirConsulta (acción de macro)
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288346"
---
# <a name="openquery-macro-action"></a>AbrirConsulta (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AbrirConsulta** para abrir una consulta de selección o de tabla de referencias cruzadas en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta una consulta de acción. También puede seleccionar un modo de entrada de datos para la consulta.

> [!NOTE]
> [!NOTA] Esta acción sólo está disponible en el entorno de bases de datos de Access (.mdb o .accdb). Vea las acciones **AbrirVista**, **AbrirProcedimientoAlmacenado** o **AbrirFunción** si utiliza el entorno de proyectos de Access (.adp).

## <a name="setting"></a>Configuración

La acción **AbrirConsulta** tiene los siguientes argumentos.

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
<td><p><strong>Nombre de la consulta</strong></p></td>
<td><p>Nombre de la consulta que se va a abrir. El <strong>cuadro Nombre de</strong> consulta de la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las consultas de la base de datos actual. Este es un argumento obligatorio. Si ejecuta una macro que contiene la acción <strong>OpenQuery</strong> en una base de datos de biblioteca, Microsoft Access primero busca la consulta con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Vista en la que se va a abrir la consulta. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>Modo de entrada de datos de la consulta. Esto sólo se aplica a las consultas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede modificar los existentes), <strong>Modificar</strong> (el usuario puede modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si usa **Hoja de datos** para el argumento **Vista**, Access muestra el conjunto de resultados si la consulta es una consulta de selección, de tabla de referencias cruzadas, de combinación o de paso a través cuya propiedad **DevuelveRegistros** está establecida en **Sí** y ejecuta la consulta si es una consulta de acción, de definición de datos o de paso a través cuya propiedad **DevuelveRegistros** está establecida en **No**.

La acción **AbrirConsulta** es similar a hacer doble clic en la consulta en el panel de navegación o hacer clic con el botón secundario en la consulta en el panel de navegación y seleccionar una vista. Con esta acción, se pueden seleccionar opciones adicionales.

> [!TIP]
> - Puede arrastrar una consulta desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirConsulta** que abre la consulta en la vista Hoja de datos. Al cambiar a la vista Diseño mientras está abierta la consulta, se quita el valor del argumento **Modo de datos** de la consulta. Este valor no tiene efecto, incluso si el usuario vuelve a la vista Hoja de datos.
> - Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una consulta de acción (que indican que es una consulta de acción y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.

Para ejecutar la acción **AbrirConsulta** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenQuery** del objeto **DoCmd**.

