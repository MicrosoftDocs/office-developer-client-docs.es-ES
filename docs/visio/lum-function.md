---
title: LUM (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Devuelve el valor del componente de luminosidad de un color.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822564"
---
# <a name="lum-function"></a>LUM (función)

Devuelve el valor del componente de luminosidad de un color.
  
## <a name="syntax"></a>Sintaxis

LUM (** *expresión* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de un color en la tabla de colores del documento o una referencia a una celda que contiene un índice de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

El valor devuelto es un número en el intervalo de 0 a 240, ambos incluidos. La función devuelve 0 para la entrada no válida. 
  
## <a name="example-1"></a>Ejemplo 1

¡LUM (hoja.4! FillForegnd)
  
Devuelve la luminosidad del color de relleno del primer plano en la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

LUM(6)
  
Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 6 está asignado al color magenta.
  
## <a name="example-3"></a>Ejemplo 3

LUM(HSL(10; 20; 30))
  
Devuelve 30.
  

