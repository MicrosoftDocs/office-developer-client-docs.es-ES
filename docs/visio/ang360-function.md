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
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160303"
---
# <a name="ang360-function"></a>Función ANG360

Normaliza el rango de un ángulo en 0 = radianes 2PI de resultado \< \< (0 \< = resultado \< 360 grados).
  
## <a name="syntax"></a>Sintaxis

ANG360(***angle*** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _ángulo_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El ángulo que se normalizará.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si  *el*  ángulo no se especifica mediante unidades angulares, se interpreta como radianes. Si  *el*  ángulo no se puede convertir en un valor, #VALUE! error se devuelve. 
  
## <a name="example-1"></a>Ejemplo 1

ANG360(395 grad)
  
Devuelve 35 grad
  
## <a name="example-2"></a>Ejemplo 2

ANG360(-9,8 rad)
  
Devuelve 2,7664 rad
  
## <a name="example-3"></a>Ejemplo 3

ANG360(45)
  
Devuelve 58,31 grad (1,0177 rad)
  

