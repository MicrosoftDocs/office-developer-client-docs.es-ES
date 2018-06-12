---
title: ANG360 (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normaliza el intervalo de un ángulo.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821521"
---
# <a name="ang360-function"></a>ANG360 (función)

Normaliza el intervalo de un ángulo para que sea 0 \<= resultado \< 2 pi radianes (0 \<= resultado \< 360 grados).
  
## <a name="syntax"></a>Sintaxis

ANG360 (** *ángulo* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _ángulo_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El ángulo que se normalizará.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si no se especifica el *ángulo* mediante el uso de unidades angulares, se interpreta como radianes. Si el *ángulo* no se puede convertir en un valor, #VALUE! se devuelve el error. 
  
## <a name="example-1"></a>Ejemplo 1

ANG360(395 grad)
  
Devuelve 35 grad
  
## <a name="example-2"></a>Ejemplo 2

ANG360(-9,8 rad)
  
Devuelve 2,7664 rad
  
## <a name="example-3"></a>Ejemplo 3

ANG360(45)
  
Devuelve 58,31 grad (1,0177 rad)
  

