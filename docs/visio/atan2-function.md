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
description: Devuelve el ángulo entre el vector representado por x, y y la dirección de la x-eje. El resultado es un número en la unidad actual de medida para los ángulos.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821526"
---
# <a name="atan2-function"></a>ATAN2 (función)

Devuelve el ángulo entre el vector representado por *x, y* y la dirección de la *x* -eje. El resultado es un número en la unidad actual de medida para los ángulos. 
  
## <a name="syntax"></a>Sintaxis

ATAN2 (** *y* **, ** *x* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |La _y_-valor del punto.  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |La _x_-valor del punto.  <br/> |
   
## <a name="remarks"></a>Notas

El arco tangente es el ángulo ascendente medido desde el positivo *x* -eje a una línea que cruza el origen (0,0) y el punto representado por *x* e *y* . En Microsoft Visio, ATAN2(0,0) devuelve 0. Para forzar el resultado de ATAN2 en una medida angular distinta, utilice la función DEG o RAD. 
  
La función ATAN2 es la inversa de la función TAN. La función ATAN2 Devuelve el ángulo cuya tangente es igual a *y* dividido entre *x* . Si ATAN2 (*y, x*) representa un ángulo en un triángulo rectángulo, *y* es el "lado opuesto" y *x* es el "lado adyacente", por lo que la función podría escribirse como ATAN2(opposite,adjacent). 
  
## <a name="example-1"></a>Ejemplo 1

ATAN2(1.25,2.25)
  
Devuelve 29,0456 grados.
  
## <a name="example-2"></a>Ejemplo 2

ATAN2(1;SQRT(3))
  
Devuelve 30 grados.
  
## <a name="example-3"></a>Ejemplo 3

ATAN2(1;1)
  
Devuelve 45 grados.
  

