---
title: Acción de macro SetReturnVar (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: La acción SetReturnVar crea una variable de devolución y la establece en un valor específico.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409597"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>Acción de macro SetReturnVar (aplicación web personalizada de Access)

La **acción SetReturnVar** crea una variable de devolución y la establece en un valor específico. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> La **acción SetReturnVar** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Setting

La **acción SetReturnVar** tiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| _Name_ <br/> |Sí  <br/> |Una cadena que especifica el nombre de la variable.  <br/> |
| _Expression_ <br/> |Sí  <br/> |Una expresión que se utilizará para establecer el valor de esta variable temporal. No anteponga el signo igual (=) a la expresión. Puede hacer clic en el botón **Generar** para utilizar el **Generador de expresiones** para establecer este argumento.  <br/> |
   
## <a name="remarks"></a>Comentarios

La **acción SetReturnVar** se usa para crear un **ReturnVar**, que es una variable que pueden usar las macros que llaman a una macro de datos mediante la acción **RunDataMacro.** 
  
Después de **crear un ReturnVar** mediante la acción **SetReturnVar,** la macro que llama puede usarla en una expresión. Por ejemplo, si creó un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable mediante la siguiente sintaxis:
  
`=[ReturnVars]![UpdateSuccess]`

La **acción SetReturnVar** sólo se puede usar en macros de datos con nombre. No está disponible en macros de datos adjuntas a un evento de macro de datos. 
  

