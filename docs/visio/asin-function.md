---
title: ASIN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Devuelve el arcoseno de un número; por ejemplo, el ángulo cuyo seno es número.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341527"
---
# <a name="asin-function"></a>Función ASIN

Devuelve el arcoseno de un número; por ejemplo, el ángulo cuyo seno es *número* . 
  
## <a name="syntax"></a>Sintaxis

ASENo (* * *número* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El seno del ángulo.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de entrada debe estar en el intervalo-1 < = *número* < = 1, o un #NUM! se devuelve un error. El ángulo resultante está en el intervalo-PI/2 < = *Angle* _LT_ = pi/2 radianes (-90 < = *angle* < = 90 grados). 
  
## <a name="example"></a>Ejemplo

ASENO (1)
  
Devuelve 90 grados.
  

