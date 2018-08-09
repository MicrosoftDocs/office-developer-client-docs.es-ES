---
title: BITAND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario 1 y númeroBinario2 es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821627"
---
# <a name="bitand-function"></a>Función BITAND

Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario 1 y númeroBinario2 es 1. De lo contrario, el bit se establece en 0. 
  
## <a name="syntax"></a>Sintaxis

BITAND (** *número binario 1* **, ** *númeroBinario2* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario 1_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El primer número binario de 16 bits.  <br/> |
| _número binario 2_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El segundo número binario de 16 bits.  <br/> |
   
## <a name="remarks"></a>Observaciones

Puede usar esta función para probar y cambiar las propiedades de una forma que se almacenan como máscaras de bits, por ejemplo, el formato de texto de la forma.
  
## <a name="example"></a>Ejemplo

BITAND(12;6)
  
Devuelve 4. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITAND(12,6) = 0...00100.
  

