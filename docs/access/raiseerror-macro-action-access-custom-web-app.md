---
title: Acción de macro RaiseError (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: La acción ProvocarError muestra una ventana emergente que contiene un mensaje de error especificado.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408246"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a>Acción de macro RaiseError (aplicación web personalizada de Access)

La **acción ProvocarError** muestra una ventana emergente que contiene un mensaje de error especificado. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> La acción **ProvocarError** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Setting

La **acción ProvocarError** tiene el siguiente argumento. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
| _Descripción del error_ <br/> |Una expresión de cadena que describe el error.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se **llama a la** acción ProvocarError, se revierte todas las operaciones de la transacción actual. 
  

