---
title: QuitarVariableTemporal (acción de macro)
TOCTitle: RemoveTempVar Macro Action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 61d03f23e0fbe04cae49670366f76c02e81d694a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485533"
---
# <a name="removetempvar-macro-action"></a>QuitarVariableTemporal (acción de macro)


**Se aplica a**: Access 2013 | Office 2013



Puede usar la acción **QuitarVariableTemporal** para quitar una sola variable temporal creada mediante la acción **DefinirVariableTemporal**.

## <a name="setting"></a>Configuración

La acción **QuitarVariableTemporal** tiene el siguiente argumento.

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
<td><p><strong>Name</strong></p></td>
<td><p>Especifique el nombre de la variable temporal que desee quitar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - Puede haber hasta 255 variables temporales definidas a la vez. Si no se quita una variable temporal, se mantiene en la memoria hasta que se cierre la base de datos. Se recomienda quitar las variables temporales cuando termine de usarlas.

  - Access quita automáticamente todas las variables temporales cuando se cierra la base de datos o el proyecto.

  - Si está mal escrito el nombre de la variable que se desea quitar, Access no muestra ningún error. La variable en cuestión permanecerá en la memoria hasta que se cierre la base de datos.

  - Si ha creado más de una variable temporal y desea quitarlas todas a la vez, use la acción **QuitarTodasLasVariablesTemporales**.

  - Para ejecutar la acción **QuitarVariableTemporal** en un módulo de VBA, use el método **Remove** del objeto **TempVars**.

## <a name="example"></a>Ejemplo

En la siguiente macro se muestra cómo crear una variable temporal, cómo usarla en una condición y un cuadro de mensaje y, a continuación, cómo quitarla mediante la acción **QuitarVariableTemporal**.

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
<td><p><strong>DefinirVariableTemporal</strong></p></td>
<td><p><strong>Nombre</strong>: MiVar<strong>expresión</strong>: CuadroEntr (&quot;escriba un número distinto de cero.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: =&quot;ha escrito &quot; &amp; [variables temporales]! [MiVar] &amp; &quot;. &quot; <strong>Bip</strong>: <strong>YesType</strong>: <strong>información</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>QuitarVariableTemporal</strong></p></td>
<td><p><strong>Nombre</strong>: MiVar</p></td>
</tr>
</tbody>
</table>

