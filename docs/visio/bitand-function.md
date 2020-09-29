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
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 sólo si el bit correspondiente en binarynumber1 y binarynumber2 es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293495"
---
# <a name="bitand-function"></a>Función BITAND

Devuelve un número binario de 16 bits en el que cada bit se establece en 1 sólo si el bit correspondiente en binarynumber1 y binarynumber2 es 1. De lo contrario, el bit se establece en 0. 
  
## <a name="syntax"></a>Sintaxis

BITAND (***binarynumber1***, ***binarynumber2*** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario_ <br/> |Necesario  <br/> |**Numérico** <br/> |El primer número binario de 16 bits.  <br/> |
| _número2 binario_ <br/> |Necesario  <br/> |**Numérico** <br/> |El segundo número binario de 16 bits.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar esta función para probar y cambiar las propiedades de una forma que se almacenan como máscaras de bits, por ejemplo, el formato de texto de la forma.
  
## <a name="example"></a>Ejemplo

BITAND (12, 6)
  
Devuelve 4. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITAND(12,6) = 0...00100.
  

