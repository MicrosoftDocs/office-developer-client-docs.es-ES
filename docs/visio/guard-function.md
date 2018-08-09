---
title: GUARD (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protege la expresión de eliminar ni cambiar mediante acciones realizadas en la ventana de dibujo, por ejemplo, mover, cambiar de tamaño, agrupar o desagrupar formas.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822247"
---
# <a name="guard-function"></a>Función GUARD

Protege la *expresión* de eliminar ni cambiar mediante acciones realizadas en la ventana de dibujo, por ejemplo, mover, cambiar de tamaño, agrupar o desagrupar formas. 
  
## <a name="syntax"></a>Sintaxis

GUARD (** *expresión* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a las celdas de ShapeSheet que da como resultado un valor.  <br/> |
   
## <a name="remarks"></a>Observaciones

Las celdas con que se suele utilizar la función GUARD son Width, Height, PinX y PinY. 
  
Al guardar una fórmula en una celda se impide que pueda cambiar el valor de esa celda como consecuencia de acciones realizadas en la ventana de dibujo. Sin embargo, una acción efectuada en la ventana de dibujo puede afectar a varias celdas, por lo que todas ellas deben estar protegidas por la función GUARD si desea evitar cambios inesperados en la apariencia de la forma. 
  
## <a name="example"></a>Ejemplo

GUARD(TEXTWIDTH(TheText) + 1,5 cm) 
  
Al incluir esta expresión en la celda Width de la sección de transformación de forma se impide que la expresión (TEXTWIDTH(TheText) + 1,5 cm) sea sustituida por otro valor al cambiar el ancho de la forma en la ventana de dibujo. TheText es una celda que se desencadena cuando cambia la composición del texto de la forma asociada. 
  

