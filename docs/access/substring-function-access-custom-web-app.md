---
title: Función SubString (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve parte de una expresión de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433475"
---
# <a name="substring-function-access-custom-web-app"></a>Función SubString (aplicación web personalizada de Access)

Devuelve parte de una expresión de texto.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
La **función SubString** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Expresión de texto.  <br/> |
| *Start*  <br/> |Expresión de entero que especifica dónde comienzan los caracteres devueltos. Si start es menor que 1, la expresión devuelta empezará en el primer carácter especificado en expresión. En este caso, el número de caracteres devueltos es el valor más grande de la suma de start + length- 1 o 0. Si start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.  <br/> |
| *Length*  <br/> |Expresión de entero positivo que especifica cuántos caracteres de la expresión se devolverán. Si la longitud es negativa, se genera un error y se termina la instrucción. Si la suma de inicio y longitud es mayor que el número de caracteres de expresión, se devuelve toda la expresión de valor que comienza al principio.  <br/> |
   

