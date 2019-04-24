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
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en el número binario número1 o el número binario 2 es 1. El bit se establece en 0 sólo si el bit correspondiente es 0 en el argumento número1 binario y el número binario 2.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303377"
---
# <a name="bitor-function"></a>Función BITOR

Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en el *número binario número1* o el número *binario 2* es 1. El bit se establece en 0 sólo si el bit correspondiente es 0 en el argumento *número1 binario* y el número binario *2* . 
  
## <a name="syntax"></a>Sintaxis

BITOR (* * *número binario* 1 * *, * * número *binario 2* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _número binario_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El primer número binario de 16 bits.  <br/> |
| _número2 binario_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El segundo número binario de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Binario de 16 bits
  
## <a name="example"></a>Ejemplo

BITOR (12, 6)
  
Devuelve 14. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITOR(12;6) = 0...01110.
  

