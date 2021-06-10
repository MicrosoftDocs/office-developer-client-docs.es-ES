---
title: EjecutarCódigo (acción de macro)
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306835"
---
# <a name="runcode-macro-action"></a>EjecutarCódigo (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **EjecutarCódigo** para llamar a un procedimiento Function de Visual Basic para Aplicaciones (VBA).

## <a name="setting"></a>Configuración

La acción **EjecutarCódigo** utiliza el siguiente argumento.

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
<td><p><strong>Nombre de función</strong></p></td>
<td><p>Nombre del procedimiento Function de VBA que va a ejecutarse. Encierre entre paréntesis los argumentos de la función. Especifique el nombre de la función en el cuadro <strong>Nombre de función</strong> situado en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.  </p><p><strong>NOTA</strong>: en una base de datos de Access <strong></strong> (.mdb o .accdb), haga clic en el botón Generar para usar el Generador de expresiones para seleccionar una función para este argumento. Haga clic en la función deseada de la lista del Generador de expresiones.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Los procedimientos de función definidos por usuario se almacenan en módulos de Microsoft Access.

Debe incluir paréntesis, incluso si el procedimiento de función no tiene ningún argumento, como en el siguiente ejemplo:

`TestFunction()`

A diferencia de los nombres de función definidos por el usuario usados para la configuración de propiedades de evento, el nombre de la función en el argumento **Nombre** de función no comienza con un signo igual ( **=** ).

Access no utiliza el valor devuelto por la función.

> [!NOTE]
> No podrá llamar a un procedimiento Function desde una macro si el nombre de la función coincide con el del módulo.

> [!TIP]
> [!SUGERENCIA] Para ejecutar un procedimiento Sub o un procedimiento de evento escrito en Visual Basic, cree un procedimiento de función que llama al procedimiento Sub o al procedimiento de evento. A continuación, utilice la acción **EjecutarCódigo** para ejecutar el procedimiento de función.

Si utiliza la acción **EjecutarCódigo** para llamar a una función, Access busca la función especificada por el argumento **Nombre de función** en los módulos estándar de la base de datos. Sin embargo, cuando esta acción se ejecuta como respuesta a la elección de un comando de menú de un formulario o informe, o como respuesta a un evento de un formulario o informe, Access busca primero la función en el módulo de clases del formulario o informe y, después, en los módulos estándar. Access no busca la función especificada por el argumento **Nombre de función** en los módulos de clases que aparecen en el área **Módulos** del panel de navegación.

Esta acción no está disponible para módulos de VBA. En su lugar, ejecute el procedimiento de función que desee directamente en VBA.

