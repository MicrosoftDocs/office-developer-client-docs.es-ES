---
title: ISERRVALUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Devuelve TRUE si el valor de cellreference es el tipo de error #VALUE, donde un argumento de la fórmula es el tipo incorrecto. La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404431"
---
# <a name="iserrvalue-function"></a>Función ISERRVALUE

Devuelve TRUE si el valor de  _cellreference_ es el tipo de error #VALUE, donde un argumento de la fórmula es el tipo incorrecto. La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas A a D de borrador no devuelven nuca un error #VALUE! ya que sus fórmulas pueden contener números y letras dentro de la misma cadena. Las celdas de la X a la Y deben contener sólo números. 
  
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Fórmula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Devuelve 2 ya que el valor devuelto es un error del tipo #VALUE! y la expresión indica a Microsoft Visio que debe devolver un 2 en lugar del error.
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Fórmula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Devuelve 12 ya que el valor devuelto no es un error del tipo #VALUE! y la expresión indica a Visio que debe devolver el valor de la celda original.
  

