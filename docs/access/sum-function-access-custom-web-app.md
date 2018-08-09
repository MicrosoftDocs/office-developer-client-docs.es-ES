---
title: Función SUM (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Devuelve la suma de todos los valores de la expresión.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815504"
---
# <a name="sum-function-access-custom-web-app"></a>Función SUM (aplicación web personalizado de Access)

Devuelve la suma de todos los valores de la expresión.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Suma** (*NumericExpression*) 
  
La función **Sum** contiene el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *NumericExpression*  <br/> |Una expresión que identifica el campo que contiene los datos numéricos que desea agregar o una expresión que realiza un cálculo utilizando los datos de ese campo. Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).  <br/> |
   
## <a name="remarks"></a>Comentarios

La función **Sum** omite los registros que contienen valores nulos. 
  
La función **Sum** sólo puede utilizarse con columnas numéricas. 
  

