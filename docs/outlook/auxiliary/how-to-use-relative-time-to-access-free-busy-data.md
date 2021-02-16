---
title: Usar tiempo relativo para obtener acceso a los datos de disponibilidad
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: La interfaz IFreeBusyData de la API de disponibilidad usa un concepto de tiempo relativo, que es el número de minutos desde el 1 de enero de 1601, expresado en hora universal (UTC), y es un valor de tipo LONG .
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317636"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Usar tiempo relativo para obtener acceso a los datos de disponibilidad

La interfaz [IFreeBusyData](ifreebusydata.md) de la API de disponibilidad usa un concepto de tiempo relativo, que es el número de minutos desde el 1 de enero de 1601, expresado en hora universal (UTC), y es un valor de tipo **LONG**. 
  
Estos son algunos valores de tiempo relativo que se usan habitualmente:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Use los valores de tiempo relativo mínimo y máximo anteriores para ayudar a comprobar que los valores de tiempo relativo son válidos.
  
Dado que NTFS registra las horas de archivo de forma nativa en formato [FILETIME,](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) puede ser útil usar el siguiente ejemplo de código para convertir el tiempo relativo a y desde **FILETIME**. 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>Consulte también

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

