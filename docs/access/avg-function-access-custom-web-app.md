---
title: Función AVG (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426726"
---
# <a name="avg-function-access-custom-web-app"></a>Función AVG (aplicación web personalizada de Access)

Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **PROM** (*NumericExpression*) 
  
La función **AVG** contiene el siguiente argumento. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|NumericExpression  <br/> |Una expresión de cadena que identifica el campo que contiene los datos numéricos que desea calcular como promedio o una expresión que realiza un cálculo con los datos de ese campo. Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una variable o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).  <br/> |
   
## <a name="remarks"></a>Comentarios

El promedio calculado por **Avg** es la media aritmética (la suma de los valores dividida entre el número de valores). **Avg** de puede usar, por ejemplo, para calcular el promedio del costo de transporte. 
  
La función **AVG** no incluye ningún valor **null** en el cálculo. 
  

