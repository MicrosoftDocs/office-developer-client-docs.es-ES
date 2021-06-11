---
title: OR (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina dos condiciones. Devuelve TRUE cuando cualquiera de las dos condiciones es true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414763"
---
# <a name="or-access-custom-web-app"></a>OR (aplicación web personalizada de Access)

Combina dos condiciones. Devuelve TRUE cuando cualquiera de las dos condiciones es true.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *BooleanExpression* **o** *BooleanExpression* 
  
El **operador Or** usa el argumento siguiente. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Cualquier expresión válida que devuelva TRUE o FALSE.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se usa más de un operador lógico en una instrucción, los operadores **Or** se evalúan después de **los operadores And.** Sin embargo, puede cambiar el orden de evaluación mediante paréntesis. 
  
En la tabla siguiente se muestra el resultado del **operador Or.** 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

