---
title: HUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Devuelve el valor del componente de matiz de un color.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822296"
---
# <a name="hue-function"></a>HUE (función)

Devuelve el valor del componente de matiz de un color.
  
## <a name="syntax"></a>Sintaxis

MATIZ (** *expresión* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión que da como resultado un color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

El valor obtenido es un número en el intervalo de 0 a 239, ambos incluidos. La entrada es el índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color. La función devuelve 0 si la entrada no es válida. 
  
## <a name="example-1"></a>Ejemplo 1

¡MATIZ (hoja.4! FillForegnd)
  
Devuelve el matiz del color de relleno en primer plano de la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

HUE(7)
  
Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Microsoft Visio, en la que el índice 7 está asignado al color cian.
  
## <a name="example-3"></a>Ejemplo 3

HUE(HSL(10; 20; 30) )
  
Devuelve 10.
  

