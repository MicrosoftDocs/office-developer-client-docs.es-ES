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
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439495"
---
# <a name="hue-function"></a>Función HUE

Devuelve el valor del componente de matiz de un color.
  
## <a name="syntax"></a>Sintaxis

HUE(** *expression* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión que da como resultado un color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

El valor obtenido es un número en el intervalo de 0 a 239, ambos incluidos. La entrada es el índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color. La función devuelve 0 si la entrada no es válida. 
  
## <a name="example-1"></a>Ejemplo 1

HUE(Sheet.4! FillForegnd)
  
Devuelve el matiz del color de relleno en primer plano de la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

HUE(7)
  
Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Microsoft Visio, en la que el índice 7 está asignado al color cian.
  
## <a name="example-3"></a>Ejemplo 3

HUE(HSL(10; 20; 30) )
  
Devuelve 10.
  

