---
title: Función Choose (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Devuelve el elemento en el índice especificado de una lista de valores.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414119"
---
# <a name="choose-function-access-custom-web-app"></a>Función Choose (aplicación web personalizada de Access)

Devuelve el elemento en el índice especificado de una lista de valores.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**Elige** (*IndexNumber*, *Value*, [*Value_n*]) 
  
La función **Choose** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *IndexNumber*  <br/> |Expresión de tipo Integer que representa un índice de base 1 en la lista de los elementos que le siguen.  <br/> |
| *Valor*  <br/> |Lista de valores de cualquier tipo de datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el *IndexNumber* proporcionado no es un entero, el valor se convierte implícitamente en un entero. 
  
Si el valor de índice supera los límites de la matriz de valores, **Choose** devuelve NULL. 
  

