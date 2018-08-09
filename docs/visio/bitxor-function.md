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
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en alguno, pero no ambos número binario 1 o número binario 2 es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821638"
---
# <a name="bitxor-function"></a>Función BITXOR

Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en alguno, pero no ambos número binario 1 o número binario 2 es 1. De lo contrario, el bit se establece en 0.
  
## <a name="syntax"></a>Sintaxis

BITXOR (** *número binario 1* **, ** *número binario 2* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario 1_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El primer número binario de 16 bits.  <br/> |
| _número binario 2_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El segundo número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITXOR(12;6)
  
Devuelve 10. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITXOR(12,6) = 0...01010.
  

