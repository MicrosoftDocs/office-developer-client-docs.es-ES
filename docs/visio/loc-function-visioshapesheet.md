---
title: LOC (función) (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Toma un punto definido en las coordenadas locales de la uno forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada con la fórmula.
ms.openlocfilehash: 196e2c92ea6ab410b6ecca9767b68605e4eb4d30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822492"
---
# <a name="loc-function-visioshapesheet"></a>LOC (función) (VisioShapeSheet)

Toma un punto definido en las coordenadas locales de la uno forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada con la fórmula. 
  
## <a name="syntax"></a>Sintaxis

LOC (** *Elija* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _punto_ <br/> |Obligatorio  <br/> |**String** <br/> | Un punto definido en una de las coordenadas locales de la forma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Observaciones

Las coordenadas locales se miden desde la esquina inferior izquierda del rectángulo de selección de la forma. Ambas formas deben estar en la misma página.
  
## <a name="example"></a>Ejemplo

¡LOC (PNT (hoja.5! ¡LocPinX, hoja.5! LocPinY)) 
  
En esta expresión, PNT convierte un conjunto de coordenadas locales de Hoja.5 en un punto (Hoja.5 es otra forma que se encuentra en la misma página de dibujo). LOC convierte a continuación ese punto en un punto equivalente del sistema de coordenadas locales de la forma actual, en relación con la esquina inferior izquierda del rectángulo de selección de la forma actual. 
  
El número 5 de hoja.5 es el número de identificador de la forma, que se muestra en el cuadro de diálogo **Nombre de la forma** (ficha**Programador** ). 
  

