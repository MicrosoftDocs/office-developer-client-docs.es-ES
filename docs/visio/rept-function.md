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
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823005"
---
# <a name="rept-function"></a>Función REPT

Repite el texto un número determinado de veces. 
  
## <a name="syntax"></a>Sintaxis

REPT (** *texto* **, ** *veces* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto que se desea repetir.  <br/> |
| _número de veces_ <br/> |Obligatorio  <br/> |**Número** <br/> |Número positivo que indica las veces que debe aparecer el texto.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si *veces* es: 
  
- cero (0), REPT devuelve "" (ningún texto).
    
- Un número no entero, se redondea a la baja.
    
## <a name="example"></a>Ejemplo

REPT ("\*", 5) 
  
Devuelve \* \* \* \* \*. 
  

