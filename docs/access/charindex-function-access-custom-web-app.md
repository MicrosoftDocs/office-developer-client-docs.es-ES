---
title: Función CharIndex (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Busca en una expresión de texto otra expresión de texto y devuelve su posición inicial si se encuentra.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423135"
---
# <a name="charindex-function-access-custom-web-app"></a>Función CharIndex (aplicación web personalizada de Access)

Busca en una expresión de texto otra expresión de texto y devuelve su posición inicial si se encuentra.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Nombre del argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Sí  <br/> |Expresión de texto que contiene el texto que se va a encontrar.  <br/> |
| *WithinText*  <br/> |Sí  <br/> |Expresión de texto que se va a buscar.  <br/> |
| *Start*  <br/> |No  <br/> |Entero que especifica la ubicación en  *WithinText*  para iniciar la búsqueda. Si  *no*  se especifica Start, es un número negativo o es 0, la búsqueda comienza al principio de  *WithinText*  .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si  *TextExpression*  o  *WithinText*  es NULL,  *CharIndex*  devuelve NULL. 
  
Si  *TextExpression*  no se encuentra en  *WithinText*,  *CharIndex*  devuelve 0. 
  
La posición inicial devuelta es basada en 1, no en 0.
  

