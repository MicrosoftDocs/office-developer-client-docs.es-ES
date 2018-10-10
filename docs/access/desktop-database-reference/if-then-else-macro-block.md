---
title: Si...Entonces...Sino (bloque de macro)
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79e5379ad2c50eff3ddf12b597defc7b85cefb39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486740"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="0a741-102">Si...Entonces...Sino (bloque de macro)</span><span class="sxs-lookup"><span data-stu-id="0a741-102">If...Then...Else Macro Block</span></span>


<span data-ttu-id="0a741-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a741-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a741-104">Puede utilizar el bloque de macro **Si** para ejecutar condicionalmente un grupo de acciones, dependiendo del valor de una expresión.</span><span class="sxs-lookup"><span data-stu-id="0a741-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="0a741-105">Valores</span><span class="sxs-lookup"><span data-stu-id="0a741-105">Setting</span></span>

<span data-ttu-id="0a741-106">Los **Si** y **O si**, se requieren los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0a741-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a741-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="0a741-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0a741-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a741-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a741-109"><strong>Expresión</strong></span><span class="sxs-lookup"><span data-stu-id="0a741-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="0a741-110">La condición que se desea probar.</span><span class="sxs-lookup"><span data-stu-id="0a741-110">The condition that you wish to test.</span></span> <span data-ttu-id="0a741-111">Debe ser una expresión que se evalúa como True o False.</span><span class="sxs-lookup"><span data-stu-id="0a741-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0a741-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a741-112">Remarks</span></span>

<span data-ttu-id="0a741-p102">Cuando se selecciona el bloque de macro **Si**, aparece un cuadro de texto para que introduzca una expresión que representa la condición que desea probar. Además, aparece un cuadro combinado donde puede insertar una acción de macro, bajo la cual se muestra automáticamente el texto "Finalizar si". Si y Finalizar si delimitan un área en la que puede introducir un grupo o un bloque de acciones. El bloque solo se ejecuta si la expresión especificada es Verdadero.</span><span class="sxs-lookup"><span data-stu-id="0a741-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="0a741-p103">Para evaluar una expresión diferente cuando la primera expresión es falsa, puede hacer clic en **Agregar O si** para insertar un bloque opcional **O si**. Debe escribir una expresión que se evalúe como Verdadero o Falso. En este caso, el bloque solo se ejecuta si la expresión es verdadera y la primera expresión es falsa.</span><span class="sxs-lookup"><span data-stu-id="0a741-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="0a741-120">Puede agregar tantos bloques **O si** como desee a un bloque Si.</span><span class="sxs-lookup"><span data-stu-id="0a741-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="0a741-p104">Puede hacer clic en **Agregar Si no** para insertar un bloque **Si no** opcional. En este caso, las acciones que se insertan debajo de **Si no** forman el bloque **Si no**, que solo se ejecuta cuando no se ejecutan las acciones anteriores. Puede agregar un único bloque **Si no** a un bloque **Si**.</span><span class="sxs-lookup"><span data-stu-id="0a741-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="0a741-124">En el siguiente ejemplo de código, las acciones de macro en el primer bloque de ejecución si el valor de \[estado\] es mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="0a741-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="0a741-125">Si el valor de \[estado\] no es mayor que 0, se evalúa la expresión que sigue a **Else If** .</span><span class="sxs-lookup"><span data-stu-id="0a741-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="0a741-126">Las acciones de macro en el bloque **Else If** ejecutarán si el valor de \[estado\] es igual a 0.</span><span class="sxs-lookup"><span data-stu-id="0a741-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="0a741-127">Por último, si no se ejecuta ni el primer bloque ni el segundo bloque, se ejecutarán las acciones del bloque **Si no**.</span><span class="sxs-lookup"><span data-stu-id="0a741-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="0a741-128">Puede anidar bloques **Si**.</span><span class="sxs-lookup"><span data-stu-id="0a741-128">You can nest **If** blocks.</span></span> <span data-ttu-id="0a741-129">Considere la posibilidad de anidar un bloque **Si** en un bloque **Si** si desea evaluar una segunda expresión cuando la primera expresión es verdadera.</span><span class="sxs-lookup"><span data-stu-id="0a741-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="0a741-130">En el siguiente ejemplo de código, el bloque **If** interno sólo ejecuta cuando el valor de \[estado\] ambos es mayor que 0 *y* mayor de 100.</span><span class="sxs-lookup"><span data-stu-id="0a741-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
