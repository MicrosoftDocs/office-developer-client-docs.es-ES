---
title: Función substring (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve parte de una expresión de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301697"
---
# <a name="substring-function-access-custom-web-app"></a>Función substring (aplicación web personalizada de Access)

Devuelve parte de una expresión de texto.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Subcadena** (*TextExpression*, *Inicio*, *longitud*) 
  
La **** función Substring contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Una expresión de texto.  <br/> |
| *Start*  <br/> |Expresión de tipo Integer que especifica dónde se inician los caracteres devueltos. Si Start es menor que 1, la expresión que se devuelve comenzará en el primer carácter que se especifique en la expresión. En este caso, el número de caracteres que se devuelven es el mayor valor de la suma de Start + length-1 o 0. Si Start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.  <br/> |
| *Length*  <br/> |Expresión de número entero positivo que especifica cuántos caracteres de la expresión se van a devolver. Si length es negativo, se genera un error y se termina la instrucción. Si la suma de Start y length es mayor que el número de caracteres en la expresión, se devuelve la expresión de valor completa que comienza en Start.  <br/> |
   

