---
title: FLOOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Redondea un número hacia el valor de 0 (cero), al siguiente entero o a la siguiente instancia de Multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346182"
---
# <a name="floor-function"></a>Función FLOOR

Redondea un número hacia el valor de 0 (cero), al siguiente entero o a la siguiente instancia de _Multiple_.
  
## <a name="syntax"></a>Sintaxis

FLOOR (* * *número* * *, * * *varios* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número que desea redondear.  <br/> |
| _distintos_ <br/> |Obligatorio  <br/> |**Number** <br/> |El múltiple por el que redondear.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si no se especifica el _múltiplo_ , el número se redondea hacia 0 hasta el siguiente entero. 
  
 _Número_ y _varios_ deben tener los mismos signos o un #NUM! se devuelve un error. Si uno o _varios_ _números_ no se pueden convertir en un valor, #VALUE! se devuelve un error. Si _número_ o _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

PISO (3.7)
  
Devuelve 3.
  
## <a name="example-2"></a>Ejemplo 2

PISO (-3,7)
  
Devuelve -3.
  
## <a name="example-3"></a>Ejemplo 3

FLOOR (3,7, 0,5)
  
Devuelve 3,5.
  

