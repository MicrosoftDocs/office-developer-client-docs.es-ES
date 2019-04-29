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
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420657"
---
# <a name="sign-function"></a>Función SIGN

Devuelve un valor que representa el signo de un número. 
  
## <a name="syntax"></a>Sintaxis

SIGN (* * *Number* * *, * * *aproximación* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numérico** <br/> | El número del que desea determinar el signo.  <br/> |
| _borrosa_ <br/> |Opcional  <br/> |**Numérico** <br/> |Especifica cuánto puede diferenciarse un número de cero para seguir considerándose igual a cero.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numérico
  
## <a name="remarks"></a>Comentarios

La función SIGN devuelve 1 si el _número_ es positivo, 0 si el _número_ es cero o-1 si el _número_ es negativo. 
  
Specifyen un valor de _aproximación_ ayuda a evitar errores de roundoff de punto flotante cuando un cálculo es casi cero. Si no especifica un valor de _aproximación_ , Visio usa 1E-9 (0,000000001). Puede interesarle usar un valor distinto en el caso de cambios de escala de dibujos o cuando desee realizar una comparación exacta. 
  
## <a name="example-1"></a>Ejemplo 1

SIGN (-5)
  
Devuelve -1.
  
## <a name="example-2"></a>Ejemplo 2

SIGNO (0)
  
Devuelve 0.
  
## <a name="example-3"></a>Ejemplo 3

SIGN (0.00000000001)
  
Devuelve 0.
  
## <a name="example-4"></a>Ejemplo 4

SIGN (0.00000000001, 0)
  
Devuelve 1.
  

