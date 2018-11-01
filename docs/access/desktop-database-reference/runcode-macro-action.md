---
title: EjecutarCódigo (acción de macro)
TOCTitle: RunCode Macro Action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e06d3ebb014cc38b19e37098b217bd072af4434a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870964"
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
<td><p>Nombre del procedimiento Function de VBA que va a ejecutarse. Encierre entre paréntesis los argumentos de la función. Especifique el nombre de la función en el cuadro <strong>Nombre de función</strong> situado en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.  </p>

> [!NOTE]
> <P>En una base de datos de Access (.mdb o .accdb), haga clic en el botón <STRONG>Generar</STRONG> para utilizar el Generador de expresiones con el fin de seleccionar una función para este argumento. Haga clic en la función deseada de la lista del Generador de expresiones.</P>


<p></p></td>
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
> <P>[!NOTA] No podrá llamar a un procedimiento Function desde una macro si el nombre de la función coincide con el del módulo.</P>




> [!TIP]
> <P>[!SUGERENCIA] Para ejecutar un procedimiento Sub o un procedimiento de evento escrito en Visual Basic, cree un procedimiento de función que llama al procedimiento Sub o al procedimiento de evento. A continuación, utilice la acción <STRONG>EjecutarCódigo</STRONG> para ejecutar el procedimiento de función.</P>



Si utiliza la acción **EjecutarCódigo** para llamar a una función, Access busca la función especificada por el argumento **Nombre de función** en los módulos estándar de la base de datos. Sin embargo, cuando esta acción se ejecuta como respuesta a la elección de un comando de menú de un formulario o informe, o como respuesta a un evento de un formulario o informe, Access busca primero la función en el módulo de clases del formulario o informe y, después, en los módulos estándar. Access no busca la función especificada por el argumento **Nombre de función** en los módulos de clases que aparecen en el área **Módulos** del panel de navegación.

Esta acción no está disponible para módulos de VBA. En su lugar, ejecute el procedimiento de función que desee directamente en VBA.

