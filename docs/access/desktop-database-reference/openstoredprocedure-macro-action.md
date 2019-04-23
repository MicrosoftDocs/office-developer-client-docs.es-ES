---
title: AbrirProcedimientoAlmacenado (acción de macro)
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288311"
---
# <a name="openstoredprocedure-macro-action"></a>AbrirProcedimientoAlmacenado (acción de macro)

**Se aplica a:** Access 2013, Office 2013

En un proyecto de Access, puede utilizar la acción **AbrirProcedimientoAlmacenado** para abrir un procedimiento almacenado en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta el procedimiento almacenado especificado cuando se abre en la vista Hoja de datos. Puede seleccionar el modo de entrada de datos del procedimiento almacenado y restringir los registros que muestra el procedimiento almacenado.

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **AbrirProcedimientoAlmacenado** tiene los siguientes argumentos.

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
<td><p><strong>Nombre del procedimiento</strong></p></td>
<td><p>Nombre del procedimiento almacenado que se va a abrir. El cuadro <strong>nombre del procedimiento</strong> en la sección argumentos de <strong>acción</strong> del panel generador de macros muestra todos los procedimientos almacenados en la base de datos actual. Éste es un argumento requerido. Si ejecuta una macro que contiene la acción <strong>AbrirProcedimientoAlmacenado</strong> en una base de datos de biblioteca, Microsoft Access primero busca el procedimiento almacenado con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Vista en la que se va a abrir el procedimiento almacenado. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>Modo de entrada de datos del procedimiento almacenado. Se aplica sólo a los procedimientos almacenados que se abren en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Esta acción es similar a hacer doble clic en el procedimiento almacenado en el panel de navegación, o bien, hacer clic con el botón secundario en el procedimiento almacenado en el panel de navegación y seleccionar el comando deseado.

Si se cambia a la vista Diseño mientras está abierto el procedimiento almacenado, se quita el valor del argumento **Modo de datos** del procedimiento almacenado. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.

> [!TIP]
> - Puede arrastrar un procedimiento almacenado desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirProcedimientoAlmacenado** que abre el procedimiento almacenado en la vista Hoja de datos.
> - Si no desea que se muestren los mensajes del sistema que normalmente aparecen al ejecutarse un procedimiento almacenado (los mensajes indican que se trata de un procedimiento almacenado y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.

Para ejecutar la acción **AbrirProcedimientoAlmacenado** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenStoredProcedure** del objeto **DoCmd**.

