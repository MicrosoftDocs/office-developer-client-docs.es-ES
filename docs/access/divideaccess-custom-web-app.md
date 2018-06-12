---
title: / (Dividir) (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide un número por otro.
ms.openlocfilehash: fd5ce0f26d6ea03f14103cd76779a95ca8a34b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815350"
---
# <a name="-divide-access-custom-web-app"></a>/ (Dividir) (aplicación web personalizado de Access)

Divide un número por otro.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Syntax

 *cheques*  /  *divisor* 
  
 *cheques*  Es la expresión numérica que dividir. Puede ser cualquier expresión válida de cualquier uno de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime. 
  
 *Divisor*  Es la expresión numérica por la que se va a dividir el dividendo. Puede ser cualquier expresión válida de cualquier uno de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime. 
  
## <a name="return-type"></a>Tipo de valor devuelto

Devuelve el tipo de datos del argumento con la prioridad más alta. 
  
Si un número entero *cheques* se dividen por un *divisor* de tipo entero, el resultado es un entero que tiene cualquier parte fraccionaria del resultado truncado. 
  
## <a name="remarks"></a>Notas

El valor real devuelto por el operador / es el cociente de la primera expresión, dividida por la segunda expresión.
  

