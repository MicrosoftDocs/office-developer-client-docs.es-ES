---
title: Función exp (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Devuelve el valor exponencial de la expresión especificada.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436415"
---
# <a name="exp-function-access-custom-web-app"></a>Función exp (aplicación web personalizada de Access)

Devuelve el valor exponencial de la expresión especificada.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Exp** (*NumericExpression*) 
  
La función **exp** contiene el siguiente argumento. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expresión de tipo Double o de un tipo que se puede convertir implícitamente en Double.  <br/> |
   
## <a name="remarks"></a>Comentarios

La constante **e** (2,718281...), es la base de los logaritmos naturales. 
  
El exponente de un número es la constante **e** elevado a la potencia del número. Por ejemplo, **exp** (1,0) = e ^ 1.0 = 2.71828182845905 and **exp** (10) = e ^ 10 = 22026.4657948067. 
  
La función exponencial del logaritmo natural de un número es el propio número: **exp** (log (n)) = n. Y el logaritmo natural de la función exponencial de un número es el propio número: LOG (**exp** (n)) = n. 
  

