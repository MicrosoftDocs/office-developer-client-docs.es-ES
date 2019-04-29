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
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415526"
---
# <a name="red-function"></a>Función RED

Devuelve el componente rojo de un color. 
  
## <a name="syntax"></a>Sintaxis

RED (* * *expresión* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> |Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

El valor devuelto es un número entre 0 y 255, ambos incluidos, o una referencia a una celda que da como resultado un índice. Si la _expresión_ no es válida, esta función devuelve 0 (negro). 
  
## <a name="example-1"></a>Ejemplo 1

ROJO (22)
  
Devuelve 51 si el documento utiliza la paleta de colores predeterminada de Microsoft Office Visio, en la que el índice 22 está asignado al color gris oscuro.
  
## <a name="example-2"></a>Ejemplo 2

ROJO (Char. color)
  
Devuelve el valor del componente rojo del color actual de fuente.
  
## <a name="example-3"></a>Ejemplo 3

RED(RGB(10, 20, 30))
  
Devuelve 10.
  

