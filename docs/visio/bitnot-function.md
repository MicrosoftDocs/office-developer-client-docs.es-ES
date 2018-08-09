---
title: BITNOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario es 0. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821602"
---
# <a name="bitnot-function"></a>Función BITNOT

Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario es 0. De lo contrario, el bit se establece en 0.
  
## <a name="syntax"></a>Sintaxis

BITNOT (** *número binario* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Un número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITNOT(6)
  
Devuelve 65529. El 6 = 0...00110. Por lo tanto, BITNOT(6) = 1...11001.
  

