---
title: DefinirVariableTemporal (acción de macro)
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306527"
---
# <a name="settempvar-macro-action"></a>DefinirVariableTemporal (acción de macro)


**Se aplica a:** Access 2013, Office 2013



Puede usar la acción **DefinirVariableTemporal** para crear una variable temporal y establecerla en un valor específico. A continuación, podrá usar la variable como condición o argumento en acciones subsiguientes, o bien, usarla en otra macro, un procedimiento de evento o en un formulario o informe.

## <a name="setting"></a>Configuración

La acción **DefinirVariableTemporal** tiene los siguientes argumentos.

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
<td><p><strong>Name</strong></p></td>
<td><p>Especifique el nombre de la variable temporal.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expresión</strong></p></td>
<td><p>Escriba una expresión que se usará para establecer el valor de esta variable temporal. No anteponga la expresión con el signo igual ( <strong>=</strong> ) . Puede hacer clic en el <strong>botón Generar</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> para usar el Generador de expresiones para establecer este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- Puede haber hasta 255 variables temporales definidas a la vez. Si no quita una variable temporal, esta permanecerá en la memoria hasta que se cierre la base de datos. Se recomienda quitar las variables temporales cuando termine de usarlas. Para quitar una sola variable temporal, use la acción **[QuitarVariableTemporal](removetempvar-macro-action.md)** y establezca su argumento en el nombre de la variable temporal que quiera quitar. Si hay más de una variable temporal y quiere quitarlas todas a la vez, use la acción **QuitarTodasLasVariablesTemporales**.

- Las variables temporales son globales. Una vez creada una variable temporal, podrá referirse a la misma en un procedimiento de evento, un módulo de Visual Basic para Aplicaciones (VBA), una consulta o una expresión. Por ejemplo, si creó una variable temporal denominada *MyVar*, podría usar la variable como origen de control para un cuadro de texto mediante la sintaxis siguiente:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > En las macros, las consultas y los procedimientos de eventos, la expresión no debe ir precedida de un signo de igualdad.
 
  Asimismo, puede referirse a las variables temporales en complementos o bases de datos de referencia.

- Para ejecutar la acción **DefinirVariableTemporal** en un módulo de VBA, use el método **Add** del objeto **TempVars**.

## <a name="example"></a>Ejemplo

En la siguiente macro se muestra cómo crear una variable temporal mediante la acción **DefinirVariableTemporal**, cómo se usa la variable temporal en una condición y un cuadro de mensaje y cómo se quita la variable temporal.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condición</p></th>
<th><p>Acción</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; You entered &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Nombre</strong>: MiVar</p></td>
</tr>
</tbody>
</table>

