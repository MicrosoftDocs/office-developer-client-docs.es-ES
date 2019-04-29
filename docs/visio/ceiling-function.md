---
title: CEILING (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Redondea un número del valor 0 (cero) a la siguiente instancia de Multiple. Si no se especifica el múltiplo, el número se redondea alejándose del 0 al siguiente entero.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404130"
---
# <a name="ceiling-function"></a>Función CEILING

Redondea un número del valor 0 (cero) a la siguiente instancia de _Multiple_. Si no se especifica el _múltiplo_ , el número se redondea alejándose del 0 al siguiente entero. 
  
## <a name="syntax"></a>Sintaxis

CEILING (* * *número* * *, * * *varios* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número que desea redondear.  <br/> |
| _distintos_ <br/> |Obligatorio  <br/> |**Number** <br/> |Múltiplo al que se va a redondear.  <br/> |
   
## <a name="remarks"></a>Comentarios

 _Número_ y _varios_ deben tener los mismos signos o un #NUM! se devuelve un error. Si uno o _varios_ _números_ no se pueden convertir en un valor, #VALUE! se devuelve un error. Si _número_ o _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

TECHO (3.7)
  
Devuelve 4.
  
## <a name="example-2"></a>Ejemplo 2

TECHO (-3,7)
  
Devuelve -4.
  
## <a name="example-3"></a>Ejemplo 3

CEILING (3,7, 0,25)
  
Devuelve 3,75.
  

