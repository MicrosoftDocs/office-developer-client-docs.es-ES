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
description: Devuelve el arcoseno de un número, por ejemplo, el ángulo cuyo seno es ese número.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821562"
---
# <a name="asin-function"></a>Función ASIN

Devuelve el arcoseno de un número, por ejemplo, el ángulo cuyo seno es ese *número* . 
  
## <a name="syntax"></a>Sintaxis

ASIN (** *número* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El seno del ángulo.  <br/> |
   
## <a name="remarks"></a>Observaciones

El valor de entrada debe estar en el intervalo entre -1 < = *número* < = 1, o un #NUM! se devuelve el error. El ángulo resultante está en el intervalo -PI/2 < = *ángulo* < = PI/2 radianes (-90 < = *ángulo* < = 90 grados). 
  
## <a name="example"></a>Ejemplo

ASIN(1)
  
Devuelve 90 grados.
  

