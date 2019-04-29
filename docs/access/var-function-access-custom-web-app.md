---
title: Función Var (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Devuelve la varianza estadística de una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado de una consulta.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437759"
---
# <a name="var-function-access-custom-web-app"></a>Función Var (aplicación web personalizada de Access)

Devuelve la varianza estadística de una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado de una consulta.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Var** (*NumericExpression*) 
  
La función **var** contiene el siguiente argumento. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Una expresión de texto que identifica el campo que contiene los datos numéricos que desea evaluar o una expresión que realiza un cálculo con los datos de ese campo. Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Var** solo se puede usar con columnas numéricas. Se omiten los valores NULL. 
  

