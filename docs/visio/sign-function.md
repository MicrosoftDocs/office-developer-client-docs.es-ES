---
title: SIGN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Devuelve un valor que representa el signo de un número.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823255"
---
# <a name="sign-function"></a>Función SIGN

Devuelve un valor que representa el signo de un número. 
  
## <a name="syntax"></a>Sintaxis

Inicio de sesión (** *número* **, ** *exploración de vulnerabilidades* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numeric** <br/> | El número del que desea determinar el signo.  <br/> |
| _exploración de vulnerabilidades_ <br/> |Opcional  <br/> |**Numeric** <br/> |Especifica cuánto puede diferenciarse un número de cero para seguir considerándose igual a cero.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric
  
## <a name="remarks"></a>Observaciones

La función SIGN devuelve 1 si el _número_ es positivo, 0 si el _número_ es cero o -1 si el _número_ es negativo. 
  
Specifyin un valor de _aproximación_ ayuda a evitar errores de redondeo de punto flotante cuando un cálculo sea casi cero. Si no especifica un valor de _aproximación_ , Visio utiliza 1E-9 (0,000000001). Es posible que desee proporcionar un valor diferente cuando se aplica una escala dibujos o cuando desee que una comparación exacta. 
  
## <a name="example-1"></a>Ejemplo 1

SIGN(-5)
  
Devuelve -1.
  
## <a name="example-2"></a>Ejemplo 2

SIGN(0)
  
Devuelve 0.
  
## <a name="example-3"></a>Ejemplo 3

SIGN(0.00000000001)
  
Devuelve 0.
  
## <a name="example-4"></a>Ejemplo 4

SIGN(0.00000000001,0)
  
Devuelve 1.
  

