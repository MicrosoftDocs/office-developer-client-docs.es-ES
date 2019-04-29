---
title: Si... A continuación,... Bloque de macros else (aplicación web personalizada de Access)
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
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>Si... A continuación,... Bloque de macros else (aplicación web personalizada de Access)

Puede utilizar el bloque de macro **Si** para ejecutar condicionalmente un grupo de acciones, dependiendo del valor de una expresión. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a>Setting

For both **If** and ** Else If **, the following arguments are required. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
|**Expression** <br/> |La condición que desea probar. Debe ser una expresión que se evalúa como Verdadero o Falso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se selecciona el bloque de macro **Si**, aparece un cuadro de texto para que introduzca una expresión que representa la condición que desea probar. Además, aparece un cuadro combinado donde puede insertar una acción de macro, bajo la cual se muestra automáticamente el texto "Finalizar si". Si y Finalizar si delimitan un área en la que puede introducir un grupo o un bloque de acciones. El bloque solo se ejecuta si la expresión especificada es Verdadero. 
  
Para evaluar una expresión diferente cuando la primera expresión es falsa, puede hacer clic en **Agregar O si** para insertar un bloque opcional **O si**. Debe escribir una expresión que se evalúe como Verdadero o Falso. En este caso, el bloque solo se ejecuta si la expresión es verdadera y la primera expresión es falsa. 
  
Puede agregar tantos bloques **O si** como desee a un bloque Si. 
  
Puede hacer clic en **Agregar Si no** para insertar un bloque **Si no** opcional. En este caso, las acciones que se insertan debajo de **Si no** forman el bloque **Si no**, que solo se ejecuta cuando no se ejecutan las acciones anteriores. Puede agregar un único bloque **Si no** a un bloque **Si**. 
  
En el siguiente ejemplo de código, las acciones de macro en el primer bloque se ejecutan si el valor de [Estado] es mayor que 0. Si el valor de [Estado] no es mayor que 0, se evalúa la expresión que sigue a **O si**. Las acciones de macro del bloque **O si** se ejecutan si el valor de [Estado] es igual a 0. Por último, si no se ejecuta ni el primer bloque ni el segundo bloque, se ejecutarán las acciones del bloque **Si no**. 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

Puede anidar bloques **Si**. Considere la posibilidad de anidar un bloque **Si** en un bloque **Si** si desea evaluar una segunda expresión cuando la primera expresión es verdadera. En el ejemplo de código siguiente, el bloque **Si** solo se ejecuta cuando el valor de [Estado] es mayor que 0  *y*  mayor que 100. 
  

