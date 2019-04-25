---
title: If...Then...Else (bloque de macro)
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291897"
---
# <a name="ifthenelse-macro-block"></a>If...Then...Else (bloque de macro)


**Se aplica a:** Access 2013, Office 2013

Puede utilizar el bloque de macro **Si** para ejecutar condicionalmente un grupo de acciones, dependiendo del valor de una expresión.

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>Valor

Los siguientes argumentos son obligatorios tanto para **Si** como para **O si**.

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
<td><p><strong>Expression</strong></p></td>
<td><p>La condición que desea probar. Debe ser una expresión que se evalúa como Verdadero o Falso.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Cuando se selecciona el bloque de macro **Si**, aparece un cuadro de texto para que introduzca una expresión que representa la condición que desea probar. Además, aparece un cuadro combinado donde puede insertar una acción de macro, bajo la cual se muestra automáticamente el texto "Finalizar si". Si y Finalizar si delimitan un área en la que puede introducir un grupo o un bloque de acciones. El bloque solo se ejecuta si la expresión especificada es Verdadero.

Para evaluar una expresión diferente cuando la primera expresión es falsa, puede hacer clic en **Agregar O si** para insertar un bloque opcional **O si**. Debe escribir una expresión que se evalúe como Verdadero o Falso. En este caso, el bloque solo se ejecuta si la expresión es verdadera y la primera expresión es falsa.

Puede agregar tantos bloques **O si** como desee a un bloque Si.

Puede hacer clic en **Agregar Si no** para insertar un bloque **Si no** opcional. En este caso, las acciones que se insertan debajo de **Si no** forman el bloque **Si no**, que solo se ejecuta cuando no se ejecutan las acciones anteriores. Puede agregar un único bloque **Si no** a un bloque **Si**.

En el siguiente ejemplo de código, las acciones de macro en el primer bloque se ejecutan si el valor de \[Estado\] es mayor que 0. Si el valor de \[Estado\] no es mayor que 0, se evalúa la expresión que sigue a **O si**. Las acciones de macro del bloque **O si** se ejecutan si el valor de \[Estado\] es igual a 0. Por último, si no se ejecuta ni el primer bloque ni el segundo bloque, se ejecutarán las acciones del bloque **Si no**.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

Puede anidar bloques **Si**. Considere la posibilidad de anidar un bloque **Si** en un bloque **Si** si desea evaluar una segunda expresión cuando la primera expresión es verdadera. En el ejemplo de código siguiente, el bloque **Si** solo se ejecuta cuando el valor de \[Estado\] es mayor que 0 *y* mayor que 100.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
