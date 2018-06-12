---
title: Función de subcadena (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve la parte de una expresión de texto.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815506"
---
# <a name="substring-function-access-custom-web-app"></a>Función de subcadena (aplicación web personalizado de Access)

Devuelve la parte de una expresión de texto.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Syntax

 **Subcadena** (*TextExpression*, *Inicio*, *longitud*) 
  
La función de **subcadena** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Una expresión de texto.  <br/> |
| *Start*  <br/> |Una expresión de número entero que especifica dónde empezar los caracteres devueltos. Si start es menor que 1, se iniciará la expresión devuelta en el primer carácter que se especifica en la expresión. En este caso, el número de caracteres que se devuelven es el valor mayor de puede ser la suma de inicio + longitud-1 o 0. Si start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.  <br/> |
| *Length*  <br/> |Una expresión de número entero positivo que especifica cuántos caracteres de la expresión se devolverán. Si length es negativo, se genera un error y se termina la instrucción. Si la suma de start y length es mayor que el número de caracteres en expresión, se devuelve el principio de la expresión de valor todo en Inicio.  <br/> |
   

