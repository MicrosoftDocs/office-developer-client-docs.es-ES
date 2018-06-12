---
title: BITOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en número binario 1 o número binario 2 es 1. El bit se establece en 0 solo si el bit correspondiente es 0 en número binario 1 o número binario 2.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821619"
---
# <a name="bitor-function"></a>BITOR (función)

Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en *número binario 1* o *número binario 2* es 1. El bit se establece en 0 solo si el bit correspondiente es 0 en *número binario 1* o *número binario 2* . 
  
## <a name="syntax"></a>Sintaxis

BITOR (** *número binario 1* **, ** *número binario 2* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario 1_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El primer número binario de 16 bits.  <br/> |
| _número binario 2_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El segundo número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITOR(12;6)
  
Devuelve 14. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITOR(12;6) = 0...01110.
  

