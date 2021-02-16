---
title: ATAN2 (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Devuelve el ángulo entre el vector representado por x,y y la dirección del eje X. El resultado es un número en la unidad de medida angular actual.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436485"
---
# <a name="atan2-function"></a>Función ATAN2

Devuelve el ángulo entre el vector representado por *x,y* y la dirección del *eje X.* El resultado es un número en la unidad de medida angular actual. 
  
## <a name="syntax"></a>Sintaxis

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Valor  _y_ del punto.  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El  _valor x_ del punto.  <br/> |
   
## <a name="remarks"></a>Comentarios

La arco tangente es el ángulo medido en sentido contrario a las agujas del reloj desde el eje  *x*  positivo a una línea que interseca el origen (0,0) y el punto representado por  *x*  e  *y*  . En Microsoft Office Visio, ATAN2(0;0) devuelve 0. Para hacer que los resultados de ATAN2 se den en una unidad de medida angular distinta, utilice la función DEG o RAD. 
  
La función ATAN2 es la inversa de la función TAN. La función ATAN2 devuelve el ángulo cuyo ángulo es igual a  *y*  dividido por  *x*  . Si ATAN2(*y,x*) representa un ángulo en un triángulo rectángulo,  *y*  es el "lado opuesto" y  *x*  es el "lado adyacente", por lo que la función podría escribirse como ATAN2 (opuesto, adyacente). 
  
## <a name="example-1"></a>Ejemplo 1

ATAN2(1.25,2.25)
  
Devuelve 29,0456 grados.
  
## <a name="example-2"></a>Ejemplo 2

ATAN2(1,SQRT(3))
  
Devuelve 30 grados.
  
## <a name="example-3"></a>Ejemplo 3

ATAN2(1,1)
  
Devuelve 45 grados.
  

