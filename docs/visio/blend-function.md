---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mezcla dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821653"
---
# <a name="blend-function"></a>Función BLEND

Mezcla dos colores en la proporción especificada por el parámetro _float_ . 
  
## <a name="syntax"></a>Sintaxis

BLEND (** *color1* **, ** *color2* **, ** *float [0,1]* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Visio o valor RGB del primer color.  <br/> |
| _color2_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Visio o valor RGB del segundo color.  <br/> |
| _float [0,1]_ <br/> |Obligatorio  <br/> |**Float** <br/> |Proporción en la que se va a fusionar _color2_ y _color1_, respectivamente. Un número real de 0 a 1, inclusive.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

El color devuelto viene determinado por las proporciones relativas en las que se va a fusionar _color2_ y _color1_, respectivamente, como especificado por el parámetro _float_ . Por ejemplo, si _float_ es 0,25, el color devuelto está compuesta por un 75% de _color1_ y 25% de _color2_. 
  
Otra forma de tener en cuenta es que el valor _float_ se corresponde con el punto a lo largo del espectro de color desde _color1_ a _color2_. Por lo tanto, más pequeños números (más cerca de cero) para fusiones más cerca de _float_ producen a _color1_, mientras que los números más grandes (más cerca de 1) producen fusiones más cerca en _color2_.
  

