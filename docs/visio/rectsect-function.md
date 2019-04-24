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
description: Calcula el sector de un rectángulo asociado con x e y y devuelve un entero de 0 a 4, que indica el sector.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360041"
---
# <a name="rectsect-function"></a>Función RECTSECT

Calcula el sector de un rectángulo asociado con *x* e y ** y devuelve un entero de 0 a 4, que indica el sector. 
  
## <a name="syntax"></a>Sintaxis

RECTSECT (* * *ancho* * *, * * *alto* * *, * * *x* * *, * * *y* * *, * * *opción* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obligatorio  <br/> |**String** <br/> |El ancho del rectángulo.  <br/> |
| _height_ <br/> |Obligatorio  <br/> |**String** <br/> |El alto del rectángulo.  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada x.  <br/> |
| _y_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada y.  <br/> |
| _opcional_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica la forma en que deben tratarse los puntos que caen en las diagonales. Especifique el valor 0 para usar los sectores izquierdo y derecho para los puntos que forman parte de una diagonal. Especifique el valor 1 para usar los sectores superior e inferior para los puntos que forman parte de una diagonal.  <br/> |
   
## <a name="remarks"></a>Comentarios

Considere un rectángulo con un *ancho* y un *alto* , y un punto (*x, y*) desde el punto central del rectángulo. Al trazar las diagonales que unen las esquinas del rectángulo, éste queda dividido en cuatro sectores y se define su centro. Los sectores 0 al 4 representan, respectivamente, el centro del rectángulo y los sectores derecho, superior, izquierdo e inferior. 
  
![Los sectores del 0 al 4 representan respectivamente los puntos central, derecho, superior, izquierdo e inferior.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Ejemplo

RECTSECT(1 pda; 2 pda; 1 pda; -7 pda; 0) 
  
Devuelve 4. 
  

