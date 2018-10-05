---
title: RECTSECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcula el sector de un rectángulo asociado a x e y y devuelve un número entero entre 0 y 4, que indica el sector.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395087"
---
# <a name="rectsect-function"></a>Función RECTSECT

Calcula el sector de un rectángulo asociado a *x* e *y* y devuelve un número entero entre 0 y 4, que indica el sector. 
  
## <a name="syntax"></a>Sintaxis

RECTSECT (** *ancho* **, ** *alto* **, ** *x* **, ** *y* **, ** *opción* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obligatorio  <br/> |**String** <br/> |El ancho del rectángulo.  <br/> |
| _height_ <br/> |Obligatorio  <br/> |**String** <br/> |El alto del rectángulo.  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada x.  <br/> |
| _y_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada y.  <br/> |
| _opción_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica la forma en que deben tratarse los puntos que caen en las diagonales. Especifique el valor 0 para usar los sectores izquierdo y derecho para los puntos que forman parte de una diagonal. Especifique el valor 1 para usar los sectores superior e inferior para los puntos que forman parte de una diagonal.  <br/> |
   
## <a name="remarks"></a>Observaciones

Considere la posibilidad de un rectángulo que tiene un *ancho* y un *alto* y un punto (*x, y*) desde el punto central del rectángulo. Dibuja líneas diagonales a través de las esquinas del rectángulo que se va a dividir en cuatro sectores y un punto central. Los sectores 0 al 4 representan el punto central, derecha, arriba, izquierda y abajo respectivamente. 
  
![Sectores 0 al 4 representan el punto central, derecha, arriba, izquierda y abajo, respectivamente](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Ejemplo

RECTSECT(1 pda; 2 pda; 1 pda; -7 pda; 0) 
  
Devuelve 4. 
  

