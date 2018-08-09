---
title: GREEN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Devuelve el componente verde de un color.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822272"
---
# <a name="green-function"></a>Función GREEN

Devuelve el componente verde de un color.
  
## <a name="syntax"></a>Sintaxis

VERDE (** *expresión* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Varían** <br/> |Un índice de un color en la tabla de colores del documento, una expresión que se resuelve en un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un resultado de color o de índice de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

El valor devuelto es un número en el rango de 0 a 255, ambos incluidos, o una referencia de celda que se resuelve en un índice. Si la *expresión* no es válido, devuelve 0 (negro). 
  
## <a name="example-1"></a>Ejemplo 1

¡VERDE (hoja.4! FillForegnd)
  
Devuelve el componente verde del color de relleno del primer plano en la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

GREEN(11)
  
Devuelve 128 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 11 está asignado al color amarillo oscuro.
  
## <a name="example-3"></a>Ejemplo 3

GREEN(RGB(10; 20; 30))
  
Devuelve 20.
  

