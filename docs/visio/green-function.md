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
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438109"
---
# <a name="green-function"></a>Función GREEN

Devuelve el componente verde de un color.
  
## <a name="syntax"></a>Sintaxis

GREEN(** *expresión* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Índice de un color en la tabla de colores del documento, una expresión que se resuelve en un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

El valor devuelto es un número entre 0 y 255, ambos incluidos, o una referencia a una celda que da como resultado un índice. Si  *la*  expresión no es válida, devuelve 0 (negro). 
  
## <a name="example-1"></a>Ejemplo 1

GREEN(Sheet.4! FillForegnd)
  
Devuelve el componente verde del color de relleno del primer plano en la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

VERDE(11)
  
Devuelve 128 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 11 está asignado al color amarillo oscuro.
  
## <a name="example-3"></a>Ejemplo 3

GREEN(RGB(10; 20; 30))
  
Devuelve 20.
  

