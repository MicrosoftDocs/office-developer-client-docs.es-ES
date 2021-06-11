---
title: Si... A continuación... Bloque de macros Else (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Puede utilizar el bloque de macro Si para ejecutar condicionalmente un grupo de acciones, dependiendo del valor de una expresión.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434497"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="4bd3f-103">Si... A continuación... Bloque de macros Else (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="4bd3f-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="4bd3f-104">Puede utilizar el bloque de macro **Si** para ejecutar condicionalmente un grupo de acciones, dependiendo del valor de una expresión.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4bd3f-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4bd3f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bd3f-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="4bd3f-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="4bd3f-108">Setting</span></span>

<span data-ttu-id="4bd3f-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="4bd3f-110">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="4bd3f-110">**Action argument**</span></span>|<span data-ttu-id="4bd3f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4bd3f-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bd3f-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="4bd3f-112">**Expression**</span></span> <br/> |<span data-ttu-id="4bd3f-113">La condición que desea probar.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-113">The condition that you wish to test.</span></span> <span data-ttu-id="4bd3f-114">Debe ser una expresión que se evalúa como Verdadero o Falso.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bd3f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4bd3f-115">Remarks</span></span>

<span data-ttu-id="4bd3f-p103">Cuando se selecciona el bloque de macro **Si**, aparece un cuadro de texto para que introduzca una expresión que representa la condición que desea probar. Además, aparece un cuadro combinado donde puede insertar una acción de macro, bajo la cual se muestra automáticamente el texto "Finalizar si". Si y Finalizar si delimitan un área en la que puede introducir un grupo o un bloque de acciones. El bloque solo se ejecuta si la expresión especificada es Verdadero.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="4bd3f-p104">Para evaluar una expresión diferente cuando la primera expresión es falsa, puede hacer clic en **Agregar O si** para insertar un bloque opcional **O si**. Debe escribir una expresión que se evalúe como Verdadero o Falso. En este caso, el bloque solo se ejecuta si la expresión es verdadera y la primera expresión es falsa.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="4bd3f-123">Puede agregar tantos bloques **O si** como desee a un bloque Si.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="4bd3f-p105">Puede hacer clic en **Agregar Si no** para insertar un bloque **Si no** opcional. En este caso, las acciones que se insertan debajo de **Si no** forman el bloque **Si no**, que solo se ejecuta cuando no se ejecutan las acciones anteriores. Puede agregar un único bloque **Si no** a un bloque **Si**.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="4bd3f-p106">En el siguiente ejemplo de código, las acciones de macro en el primer bloque se ejecutan si el valor de [Estado] es mayor que 0. Si el valor de [Estado] no es mayor que 0, se evalúa la expresión que sigue a **O si**. Las acciones de macro del bloque **O si** se ejecutan si el valor de [Estado] es igual a 0. Por último, si no se ejecuta ni el primer bloque ni el segundo bloque, se ejecutarán las acciones del bloque **Si no**.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="4bd3f-p107">Puede anidar bloques **Si**. Considere la posibilidad de anidar un bloque **Si** en un bloque **Si** si desea evaluar una segunda expresión cuando la primera expresión es verdadera. En el ejemplo de código siguiente, el bloque **Si** solo se ejecuta cuando el valor de [Estado] es mayor que 0  *y*  mayor que 100.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

