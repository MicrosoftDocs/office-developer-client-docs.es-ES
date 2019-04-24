---
title: Función SUM (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Devuelve la suma de todos los valores de la expresión.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304238"
---
# <a name="sum-function-access-custom-web-app"></a>Función SUM (aplicación web personalizada de Access)

Devuelve la suma de todos los valores de la expresión.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Suma** (*NumericExpression*) 
  
La función **SUM** contiene el siguiente argumento. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Una expresión que identifica el campo que contiene los datos numéricos que desea agregar o una expresión que realiza un cálculo con los datos de ese campo. Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).  <br/> |
   
## <a name="remarks"></a>Comentarios

La función **SUM** omite los registros que contienen valores nulos. 
  
La función **SUM** sólo se puede usar con columnas numéricas. 
  

