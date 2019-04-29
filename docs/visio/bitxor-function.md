---
title: BITXOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 si el bit correspondiente en, pero no en el número binario 1 y el número binario 2, es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439236"
---
# <a name="bitxor-function"></a>Función BITXOR

Devuelve un número binario de 16 bits en el que cada bit se establece en 1 si el bit correspondiente en, pero no en el número binario 1 y el número binario 2, es 1. De lo contrario, el bit se establece en 0.
  
## <a name="syntax"></a>Sintaxis

BITXOR (* * *binario número1* * *, * * número *binario 2* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El primer número binario de 16 bits.  <br/> |
| _número2 binario_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El segundo número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITXOR (12, 6)
  
Devuelve 10. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITXOR(12,6) = 0...01010.
  

