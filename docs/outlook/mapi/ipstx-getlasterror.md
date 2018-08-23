---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592594"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="830f2-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="830f2-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="830f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="830f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="830f2-105">Obtiene información sobre el último error ampliada.</span><span class="sxs-lookup"><span data-stu-id="830f2-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="830f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="830f2-106">Parameters</span></span>

 <span data-ttu-id="830f2-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="830f2-107">_hResult_</span></span>
  
>  <span data-ttu-id="830f2-108">[entrada] Código de error.</span><span class="sxs-lookup"><span data-stu-id="830f2-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="830f2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="830f2-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="830f2-110">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="830f2-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="830f2-111">Esto debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="830f2-111">This must be 0.</span></span> 
    
 <span data-ttu-id="830f2-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="830f2-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="830f2-113">[out] Puntero a la estructura **MAPIERROR** que contiene la información extendida para el error.</span><span class="sxs-lookup"><span data-stu-id="830f2-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="830f2-114">Vea mapidefs.h para la definición de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="830f2-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="830f2-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="830f2-115">See also</span></span>



[<span data-ttu-id="830f2-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="830f2-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="830f2-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="830f2-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

