---
title: / (Dividir) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide un número por otro.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435190"
---
# <a name="-divide-access-custom-web-app"></a>/ (Dividir) (aplicación web personalizada de Access)

Divide un número por otro.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *dividendo*   /   *divisor* 
  
 *dividendo*  Es la expresión numérica que se va a dividir. Puede ser cualquier expresión válida de cualquiera de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime. 
  
 *Divisor*  Es la expresión numérica por la que se divide el dividendo. Puede ser cualquier expresión válida de cualquiera de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime. 
  
## <a name="return-type"></a>Tipo de valor devuelto

Devuelve el tipo de datos del argumento con mayor prioridad. 
  
Si un dividendo  *entero*  está dividido por un  *divisor*  entero, el resultado es un entero que tiene truncada cualquier parte fraccional del resultado. 
  
## <a name="remarks"></a>Comentarios

El valor real devuelto por el operador / es el cociente de la primera expresión dividida por la segunda expresión.
  

