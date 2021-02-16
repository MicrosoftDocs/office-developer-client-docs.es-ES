---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432789"
---
# <a name="blend-function"></a>Función BLEND

Combina dos colores en la proporción especificada por el _parámetro float._ 
  
## <a name="syntax"></a>Sintaxis

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de color de Visio o valor RGB del primer color.  <br/> |
| _color2_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de color de Visio o valor RGB del segundo color.  <br/> |
| _float[0,1]_ <br/> |Obligatorio  <br/> |**Float** <br/> |Proporción en la que se combinan  _color2_ y  _color1,_ respectivamente. Número real entre 0 y 1, ambos incluidos.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

El color devuelto está determinado por las proporciones relativas en las que se combinan _color2_ y _color1,_ respectivamente, según lo especificado por el _parámetro float._ Por ejemplo, si  _float_ es 0,25, el color devuelto se compone del 75 % del  _color1_ y el 25 % del  _color2_. 
  
Otra forma de pensarlo es que el valor  _flotante_ corresponde al punto a lo largo del espectro de colores de  _color1_  _a color2_. Por lo tanto, los números  más pequeños (más cercanos a cero) para los resultados flotantes se fusionan más cerca del _color1,_ mientras que los números más grandes (más cercanos a 1) producen mezclas más cercanas a _color2_.
  

