---
title: Analizar una secuencia de una propiedad binaria para leer la estructura TZREG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9e36e0d9-a28b-5978-0e23-f76e1bf506b5
description: En este tema se muestra cómo leer la estructura TZREG desde el formato persistente almacenado en la propiedad binaria PidLidTimeZoneStruct.
ms.openlocfilehash: f59251ebc980ca10f4ddce76b34e700bc430540a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317657"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure"></a>Analizar una secuencia de una propiedad binaria para leer la estructura TZREG

En este tema se muestra cómo leer la [estructura TZREG](tzreg.md) desde el formato persistente almacenado en la propiedad binaria [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).
  
```cpp
TZREG* BinToTZREG(ULONG cbReg, LPBYTE lpbReg)  
{ 
    if (!lpbReg) return NULL;  
 
    // Update this if parsing code is changed. 
    if (cbReg &amp;lt; 3*sizeof(long) + 2*sizeof(WORD) + 2*sizeof(SYSTEMTIME)) return NULL; 
 
    TZREG tzReg = {0}; 
    LPBYTE lpPtr = lpbReg; 
 
    tzReg.lBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lStandardBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lDaylightBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    lpPtr += sizeof(WORD);// reserved 
 
    tzReg.stStandardDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
    lpPtr += sizeof(WORD);// reserved 
    tzReg.stDaylightDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
 
    TZREG* ptzReg = NULL; 
    ptzReg = new TZREG; 
    if (ptzReg) 
    { 
        *ptzReg = tzReg; 
    } 
 
    return ptzReg; 
} 

```

## <a name="see-also"></a>Vea también

- [Leer las propiedades de la zona horaria en una cita](how-to-read-time-zone-properties-from-an-appointment.md)

