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
description: Devuelve la arcosina de un número, por ejemplo, el ángulo cuyo seno es número .
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293509"
---
# <a name="asin-function"></a>Función ASIN

Devuelve la arcosina de un número, por ejemplo, el ángulo cuyo seno es  *número*  . 
  
## <a name="syntax"></a>Sintaxis

ASIN(***number*** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El seno del ángulo.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de entrada debe estar en el intervalo -1 <=  *número*  <= 1, o un #NUM! error se devuelve. El ángulo resultante está en el intervalo -PI/2 <=  *ángulo*  <= PI/2 radianes (-90 <=  *ángulo*  <= 90 grados). 
  
## <a name="example"></a>Ejemplo

ASIN(1)
  
Devuelve 90 grados.
  

