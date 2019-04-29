---
title: REPT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Repite el texto un número determinado de veces.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412082"
---
# <a name="rept-function"></a>Función REPT

Repite el texto un número determinado de veces. 
  
## <a name="syntax"></a>Sintaxis

REPT (* * *texto* * *, * * *núm_de_veces* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto que se desea repetir.  <br/> |
| _veces_ <br/> |Obligatorio  <br/> |**Number** <br/> |Número positivo que indica las veces que debe aparecer el texto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si *núm_de_veces* es: 
  
- cero (0), REPT devuelve "" (ningún texto).
    
- Un número no entero, se redondea a la baja.
    
## <a name="example"></a>Ejemplo

REPT ("\*", 5) 
  
\* \*Devuelve \*. \* \* 
  

