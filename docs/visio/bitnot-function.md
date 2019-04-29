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
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 sólo si el bit correspondiente en el número binario es 0. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438837"
---
# <a name="bitnot-function"></a>Función BITNOT

Devuelve un número binario de 16 bits en el que cada bit se establece en 1 sólo si el bit correspondiente en el número binario es 0. De lo contrario, el bit se establece en 0.
  
## <a name="syntax"></a>Sintaxis

BITNOT (* * *número binario* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Un número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITNOT (6)
  
Devuelve 65529. El 6 = 0...00110. Por lo tanto, BITNOT(6) = 1...11001.
  

