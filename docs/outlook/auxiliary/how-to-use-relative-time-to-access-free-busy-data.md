---
title: Utilizar un tiempo relativo a los datos de disponibilidad de acceso
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: La interfaz de IFreeBusyData de la API de libre/ocupado usa un concepto de tiempo relativo, que es el número de minutos desde el 1 de enero de 1601, expresado en hora Universal (UTC), y es un valor de tipo LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386939"
---
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="76d12-103">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="76d12-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="76d12-104">La interfaz de [IFreeBusyData](ifreebusydata.md) de la API de libre/ocupado usa un concepto de tiempo relativo, que es el número de minutos desde el 1 de enero de 1601, expresado en hora Universal (UTC) y es un valor de tipo **LONG**.</span><span class="sxs-lookup"><span data-stu-id="76d12-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="76d12-105">Los siguientes son algunos valores de tiempo relativa usados con más frecuencia:</span><span class="sxs-lookup"><span data-stu-id="76d12-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="76d12-106">Use los valores máximo y mínimo tiempo relativo anterior para ayudar a comprobar que sus valores de tiempo relativo son válidos.</span><span class="sxs-lookup"><span data-stu-id="76d12-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="76d12-107">Debido a que NTFS de registros tiempos de archivos de forma nativa en formato [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , puede resultar útil para usar el siguiente ejemplo de código para convertir el tiempo relativo a y desde **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="76d12-107">Because NTFS records file times natively in [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="76d12-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="76d12-108">See also</span></span>

- [<span data-ttu-id="76d12-109">Información sobre la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="76d12-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="76d12-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="76d12-110">IFreeBusyData</span></span>](ifreebusydata.md)

