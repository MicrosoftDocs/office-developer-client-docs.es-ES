---
title: Función EXP (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Devuelve el valor exponencial de la expresión especificada.
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815312"
---
# <a name="exp-function-access-custom-web-app"></a>Función EXP (aplicación web personalizado de Access)

Devuelve el valor exponencial de la expresión especificada.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Exp** (*NumericExpression*) 
  
La función **Exp** contiene el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Una expresión de tipo Double o de un tipo que puede convertirse implícitamente a Double.  <br/> |
   
## <a name="remarks"></a>Comentarios

La constante **e** (2.718281...), es la base de los logaritmos naturales. 
  
El exponente de un número es la constante **e** elevado a la potencia del número. Por ejemplo **Exp** (1,0) = e ^ 1.0 = 2,71828182845905 y **Exp** (10) = e ^ 10 = 22026,4657948067. 
  
La función exponencial del logaritmo natural de un número es el número propio: **Exp** (LOG (n)) = n. Y el logaritmo natural de la función exponencial de un número es el número propio: LOG (**Exp** (n)) = n. 
  

