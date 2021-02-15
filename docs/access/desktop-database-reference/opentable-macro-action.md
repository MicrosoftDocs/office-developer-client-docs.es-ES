---
title: AbrirTabla (acción de macro)
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288297"
---
# <a name="opentable-macro-action"></a>AbrirTabla (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AbrirTabla** para abrir una tabla en la vista Hoja de datos, vista Diseño o Vista preliminar. También puede seleccionar un modo de entrada de datos para la tabla.

## <a name="setting"></a>Setting

La acción **AbrirTabla** tiene los siguientes argumentos.

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
<td><p><strong>Nombre de la tabla</strong></p></td>
<td><p>Nombre de la tabla que se va a abrir. El cuadro <strong>Nombre de la tabla</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las tablas de la base de datos activa. Éste es un argumento requerido. Si ejecuta una macro que contiene la acción <strong>AbrirTabla</strong> en una base de datos de biblioteca, Microsoft Access primero busca la tabla con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Vista en la que se va a abrir la tabla. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>Modo de entrada de datos para la tabla. Sólo se aplica a las tablas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros, pero no puede modificar los existentes), <strong>Modificar</strong> (el usuario puede modificar los registros existentes y agregar registros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Esta acción es similar a hacer doble clic en una tabla en el panel de navegación, o bien, a hacer clic con el botón secundario en la tabla en el panel de navegación y, a continuación, seleccionar una vista.

> [!TIP]
> [!SUGERENCIA] Puede arrastrar una tabla desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirTabla** que abre la tabla en la vista Hoja de datos.

Para ejecutar la acción **AbrirTabla** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenTable** del objeto **DoCmd**.

