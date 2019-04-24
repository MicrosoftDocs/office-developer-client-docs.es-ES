---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fusiona dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303300"
---
# <a name="blend-function"></a>Función BLEND

Fusiona dos colores en la proporción especificada por el parámetro _float_ . 
  
## <a name="syntax"></a>Sintaxis

BLEND (* * *color1* * *, * * *color2* * *, * * *flotante [0, 1]* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Visio o valor RGB del primer color.  <br/> |
| _color2_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Visio o valor RGB del segundo color.  <br/> |
| _punto flotante [0, 1]_ <br/> |Obligatorio  <br/> |**Float** <br/> |La proporción en la que se mezclan _color2_ y _color1_, respectivamente. Número real entre 0 y 1, ambos incluidos.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

El color devuelto está determinado por las proporciones relativas en las que se combinan _color2_ y _color1_, respectivamente, según lo especificado por el parámetro _float_ . Por ejemplo, si _float_ es 0,25, el color devuelto está compuesto 75% de _color1_ y el 25% de _color2_. 
  
Otra forma de pensar en esto es que el valor _float_ se corresponde con el punto del espectro de colores desde _color1_ hasta _color2_. Por lo tanto, los números más pequeños (más cercanos a cero) para las mezclas de alimentos de _flota_ más cerca de _color1_, mientras que los números más grandes (más cercanos a 1) producen fusiones más cercanas a _color2_.
  

