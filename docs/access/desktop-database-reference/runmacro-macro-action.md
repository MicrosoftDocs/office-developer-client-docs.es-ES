---
title: EjecutarMacro (acción de macro)
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 533ac6aff194296a9e4470e01672a8338dcbc318
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486442"
---
# <a name="runmacro-macro-action"></a>EjecutarMacro (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

Puede usar la acción **EjecutarMacro** para ejecutar una macro. La macro puede estar dentro de un grupo de macros.

Podrá usar esta acción en los siguientes casos:

  - Ejecutar una macro desde dentro de otra macro.

  - Ejecutar una macro según una condición determinada.

  - Asociar una macro a un comando de menú personalizado.

## <a name="setting"></a>Configuración

La acción **EjecutarMacro** utiliza los siguientes argumentos.

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
<td><p><strong>Nombre de macro</strong></p></td>
<td><p>Nombre de la macro que se va a ejecutar. El cuadro <strong>Nombre de la Macro</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las macros (y grupos de macros) en la base de datos actual. Si la macro se encuentra en un grupo de macros, aparece bajo el nombre del grupo de macros en la lista formato <em>nombregrupomacros</em>. <em>macroname</em>. Este argumento es obligatorio. Si ejecuta una macro que contiene la acción <strong>EjecutarMacro</strong> en una base de datos de biblioteca, Microsoft Access busca la macro con este nombre en la base de datos de biblioteca y no en la base de datos actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Número de repeticiones</strong></p></td>
<td><p>Número máximo de veces que la macro se va a ejecutar. Si deja este argumento en blanco (y el argumento <strong>Expresión de repetición</strong> también está en blanco), la macro se ejecuta una sola vez.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expresión de repetición</strong></p></td>
<td><p>Una expresión que se evalúa como <strong>Verdadero</strong> (–1) o <strong>Falso</strong> (0). La macro detiene su ejecución si la expresión se evalúa como <strong>Falso</strong>. La expresión se evalúa cada vez que se ejecuta la macro.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si escribe un nombre de grupo de macros en el argumento **Nombre de macro**, Access ejecuta la primera macro del grupo de macros.

Esta acción es similar a hacer clic en **Ejecutar macro** en la ficha **Herramientas de base de datos**, seleccionar una macro y hacer clic en **Aceptar**. Sin embargo, el comando ejecuta la macro solo una vez, mientras que la acción **EjecutarMacro** puede ejecutar una macro tantas veces como se desee.


> [!TIP]
> <P>[!SUGERENCIA] Puede usar los argumentos <STRONG>Número de repeticiones</STRONG> y <STRONG>Expresión de repetición</STRONG> para determinar cuántas veces se ejecuta la macro:</P>



  - Si deja ambos argumentos en blanco, la macro se ejecuta una vez.

  - Si especifica un número en **Número de repeticiones**, pero deja la **Expresión de repetición** en blanco, la macro se ejecuta el número de veces especificado.

  - Si deja el argumento **Número de repeticiones** en blanco, pero especifica una expresión en **Expresión de repetición**, la macro se ejecuta hasta que la expresión se evalúe como **Falso**.

  - Si especifica valores en ambos argumentos, la macro se ejecuta el número de veces que especifica el argumento **Número de repeticiones** o hasta que la **Expresión de repetición** se evalúe como **Falso** (el primer caso de los dos que se produzca).

Cuando se ejecuta una macro que contiene la acción **EjecutarMacro** y se llega a la acción **EjecutarMacro**, Access ejecuta la macro a la que se ha llamado. Cuando esta macro termina, Access vuelve a la macro original y ejecuta la acción siguiente.


> [!NOTE]
> <UL>
> <LI>
> <P>Puede llamar a una macro del mismo grupo de macros o de otro grupo de macros.</P>
> <LI>
> <P>Puede anidar macros. Es decir, puede ejecutar la macro A, que a su vez llama a la macro B, y así sucesivamente. En cada caso, cuando termina la macro a la que se ha llamado, Access regresa a la macro que efectuó la llamada y ejecuta la siguiente acción de esa macro.</P></LI></UL>



Para ejecutar la acción **EjecutarMacro** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RunMacro** del objeto **DoCmd**.

