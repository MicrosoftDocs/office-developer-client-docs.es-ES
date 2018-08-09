---
title: SAT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Devuelve el valor del componente de saturación de un color.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823099"
---
# <a name="sat-function"></a>Función SAT

Devuelve el valor del componente de saturación de un color. 
  
## <a name="syntax"></a>Sintaxis

SAT (** *expresión* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Varies** <br/> |Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric
  
## <a name="remarks"></a>Observaciones

El valor devuelto es un número en el intervalo de 0 a 240, ambos incluidos. La función devuelve 0 para la entrada no válida.
  
## <a name="example-1"></a>Ejemplo 1

¡SAT (hoja.4! FillForegnd)
  
Devuelve la saturación del color de relleno en primer plano de la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

SAT(8)
  
Devuelve 240 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 8 está asignado al color rojo oscuro.
  
## <a name="example-3"></a>Ejemplo 3

SAT(HSL(10, 20, 30))
  
Devuelve 20.
  

