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
description: 'Devuelve TRUE si el valor de referenciaDeCelda es el tipo de error #VALUE, donde un argumento de la fórmula es del tipo incorrecto. La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317890"
---
# <a name="iserrvalue-function"></a>Función ISERRVALUE

Devuelve TRUE si el valor de _referenciaDeCelda_ es el tipo de error #VALUE, donde un argumento de la fórmula es del tipo incorrecto. La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERRVALUE (* * *referenciaDeCelda* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas A a D de borrador no devuelven nuca un error #VALUE! ya que sus fórmulas pueden contener números y letras dentro de la misma cadena. Las celdas de la X a la Y deben contener sólo números. 
  
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Grietas. x1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |segundo  <br/> |
   
Devuelve 2 ya que el valor devuelto es un error del tipo #VALUE! y la expresión indica a Microsoft Visio que debe devolver un 2 en lugar del error.
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch. B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Devuelve 12 ya que el valor devuelto no es un error del tipo #VALUE! y la expresión indica a Visio que debe devolver el valor de la celda original.
  

