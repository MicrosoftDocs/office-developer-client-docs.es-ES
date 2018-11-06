---
title: AbrirFunción (acción de macro)
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a3a1ed5b08c9bf0b318baeebb7190868b90682f0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998864"
---
# <a name="openfunction-macro-action"></a>AbrirFunción (acción de macro)

**Se aplica a**: Access 2013, Office 2013

En un proyecto de Access, puede abrir la acción **AbrirFunción** para abrir una función definida por el usuario en la vista Hoja de datos, vista Diseño de función en línea, vista Editor de texto SQL (para una función escalar o una función de tabla definida por el usuario) o Vista preliminar. Esta acción ejecuta la función definida por el usuario cuando se abre en la vista Hoja de datos. También puede seleccionar el modo de entrada de datos para la función definida por el usuario y restringir los registros que muestra la función definida por el usuario.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **AbrirFunción** tiene los siguientes argumentos.

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
<td><p><strong>Nombre de función</strong></p></td>
<td><p>El nombre de la función definida por el usuario para abrir. El cuadro <strong>Nombre de la función</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las funciones definidas por el usuario en la base de datos actual. Este es un argumento requerido. Si ejecuta una macro que contiene la acción <strong>función</strong> en una base de datos de biblioteca, Microsoft Access busca primero la función con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Vista en la que se va a abrir la función definida por el usuario. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>El modo de entrada de datos para la función definida por el usuario. Esto sólo se aplica a las funciones definidas por el usuario que estén abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción es similar a hacer doble clic en una función definida por el usuario en el panel de navegación, o bien, a hacer clic con el botón secundario en la función en el panel de navegación y, a continuación, seleccionar una vista.

Si se cambia a la vista Diseño mientras está abierta la función definida por el usuario, se quita el valor del argumento **Modo de datos** de la función definida por el usuario. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.

> [!TIP]
> - Puede seleccionar una función definida por el usuario en el panel de navegación y arrastrarla hasta una fila de acción de una macro. De este modo, se crea automáticamente la acción **AbrirFunción** que abre la función definida por el usuario en la vista Hoja de datos.
> - Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una función definida por el usuario (esos mensajes indican que se trata de una función definida por el usuario y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.

Para ejecutar la acción **AbrirFunción** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenFunction** del objeto **DoCmd**.

