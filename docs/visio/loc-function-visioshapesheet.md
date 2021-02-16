---
title: Función LOC (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Toma un punto definido en las coordenadas locales de una forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada con la fórmula.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422428"
---
# <a name="loc-function-visioshapesheet"></a>Función LOC (VisioShapeSheet)

Toma un punto definido en las coordenadas locales de una forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada con la fórmula. 
  
## <a name="syntax"></a>Sintaxis

LOC(** *point* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obligatorio  <br/> |**String** <br/> | Un punto definido en una de las coordenadas locales de la forma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

Las coordenadas locales se miden desde la esquina inferior izquierda del rectángulo de selección de la forma. Ambas formas deben estar en la misma página.
  
## <a name="example"></a>Ejemplo

LOC(PNT(Sheet.5! LocPinX, Sheet.5! LocPinY)) 
  
En esta expresión, PNT convierte un conjunto de coordenadas locales de Hoja.5 en un punto (Hoja.5 es otra forma que se encuentra en la misma página de dibujo). LOC convierte a continuación ese punto en un punto equivalente del sistema de coordenadas locales de la forma actual, en relación con la esquina inferior izquierda del rectángulo de selección de la forma actual. 
  
El número 5 de Hoja.5 es el número identificador de la forma, que se muestra en el cuadro de diálogo **Nombre de forma** (en la ficha **Programador**). 
  

