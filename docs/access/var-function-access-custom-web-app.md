---
title: Función Var (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Devuelve la varianza estadística para una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado en una consulta.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815516"
---
# <a name="var-function-access-custom-web-app"></a>Función Var (aplicación web personalizado de Access)

Devuelve la varianza estadística para una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado en una consulta.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Var** (*NumericExpression*) 
  
La función **Var** contiene el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Una expresión de texto que identifica el campo que contiene los datos numéricos que desea evaluar o una expresión que realiza un cálculo utilizando los datos de ese campo. Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Var** pueden usarse con sólo columnas numéricas. Se omiten los valores nulos. 
  

