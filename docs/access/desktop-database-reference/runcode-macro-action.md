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
ms.openlocfilehash: bac15bed3b416d57f75dc7482b085478a27d5fa4
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996702"
---
# <a name="runcode-macro-action"></a>EjecutarCódigo (acción de macro)

**Se aplica a**: Access 2013, Office 2013

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
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nombre de función</strong></p></td>
<td><p>Nombre del procedimiento Function de VBA que va a ejecutarse. Encierre entre paréntesis los argumentos de la función. Especifique el nombre de la función en el cuadro <strong>Nombre de función</strong> situado en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.  </p><p><strong>Nota</strong>: base de datos de Access (.mdb o .accdb), haga clic en el botón <strong>Generar</strong> para usar el generador de expresiones para seleccionar una función para este argumento. Haga clic en la función que desee en la lista en el generador de expresiones.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Los procedimientos de función definidos por usuario se almacenan en módulos de Microsoft Access.

Debe incluir paréntesis, incluso si el procedimiento de función no tiene ningún argumento, como en el siguiente ejemplo:

`TestFunction()`

A diferencia de los nombres de función definida por el usuario usados para la configuración de la propiedad de evento, el nombre de función en el argumento **Nombre de función** no empieza con un signo igual (**=**).

Access no utiliza el valor devuelto por la función.

> [!NOTE]
> [!NOTA] No podrá llamar a un procedimiento Function desde una macro si el nombre de la función coincide con el del módulo.

> [!TIP]
> [!SUGERENCIA] Para ejecutar un procedimiento Sub o un procedimiento de evento escrito en Visual Basic, cree un procedimiento de función que llama al procedimiento Sub o al procedimiento de evento. A continuación, utilice la acción **EjecutarCódigo** para ejecutar el procedimiento de función.

Si utiliza la acción **EjecutarCódigo** para llamar a una función, Access busca la función especificada por el argumento **Nombre de función** en los módulos estándar de la base de datos. Sin embargo, cuando esta acción se ejecuta como respuesta a la elección de un comando de menú de un formulario o informe, o como respuesta a un evento de un formulario o informe, Access busca primero la función en el módulo de clases del formulario o informe y, después, en los módulos estándar. Access no busca la función especificada por el argumento **Nombre de función** en los módulos de clases que aparecen en el área **Módulos** del panel de navegación.

Esta acción no está disponible para módulos de VBA. En su lugar, ejecute el procedimiento de función que desee directamente en VBA.

