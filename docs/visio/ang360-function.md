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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417199"
---
# <a name="ang360-function"></a>Función ANG360

Normaliza el intervalo de un ángulo para que sea \<0 = \< resultado 2PI radianes ( \<0 = \< resultado 360 grados).
  
## <a name="syntax"></a>Sintaxis

ANG360 (* * *Angle* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _respecto_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El ángulo que se normalizará.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el *ángulo* no se especifica mediante el uso de unidades angulares, se interpreta como radianes. Si el *ángulo* no se puede convertir en un valor, se #VALUE! se devuelve un error. 
  
## <a name="example-1"></a>Ejemplo 1

ANG360(395 grad)
  
Devuelve 35 grad
  
## <a name="example-2"></a>Ejemplo 2

ANG360(-9,8 rad)
  
Devuelve 2,7664 rad
  
## <a name="example-3"></a>Ejemplo 3

ANG360 (45)
  
Devuelve 58,31 grad (1,0177 rad)
  

