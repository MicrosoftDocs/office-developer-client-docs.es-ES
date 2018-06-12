---
title: RED (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Devuelve el componente rojo de un color.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822900"
---
# <a name="red-function"></a>RED (función)

Devuelve el componente rojo de un color. 
  
## <a name="syntax"></a>Sintaxis

ROJO (** *expresión* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

El valor devuelto es un número en el rango de 0 a 255, ambos incluidos, o una referencia de celda que se resuelve en un índice. Si la _expresión_ no es válido, esta función devuelve 0 (negro). 
  
## <a name="example-1"></a>Ejemplo 1

RED(22)
  
Devuelve 51 si el documento utiliza la paleta de colores predeterminada de Microsoft Office Visio, en la que el índice 22 está asignado al color gris oscuro.
  
## <a name="example-2"></a>Ejemplo 2

RED(Char.color)
  
Devuelve el valor del componente rojo del color actual de fuente.
  
## <a name="example-3"></a>Ejemplo 3

RED(RGB(10, 20, 30))
  
Devuelve 10.
  

