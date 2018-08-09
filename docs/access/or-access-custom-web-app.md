---
title: O (tener acceso a la aplicación web personalizados)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina dos condiciones. Devuelve TRUE cuando alguna de las dos condiciones sea verdadera.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815461"
---
# <a name="or-access-custom-web-app"></a>O (tener acceso a la aplicación web personalizados)

Combina dos condiciones. Devuelve TRUE cuando alguna de las dos condiciones sea verdadera.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *Expresiónbooleana* **O** *Expresiónbooleana* 
  
El operador **o** utiliza el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Expresiónbooleana*  <br/> |Cualquier expresión válida que devuelve TRUE o FALSE.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se utiliza más de un operador lógico en una instrucción, se evalúan los operadores **o** después de los operadores **y** . Sin embargo, puede cambiar el orden de evaluación mediante el uso de paréntesis. 
  
En la siguiente tabla se muestra el resultado del operador **o** . 
  
||**ES TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**ES TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

