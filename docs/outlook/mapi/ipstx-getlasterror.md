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
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817953"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="05b34-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="05b34-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="05b34-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05b34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05b34-105">Obtiene información sobre el último error ampliada.</span><span class="sxs-lookup"><span data-stu-id="05b34-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="05b34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05b34-106">Parameters</span></span>

 <span data-ttu-id="05b34-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="05b34-107">_hResult_</span></span>
  
>  <span data-ttu-id="05b34-108">[entrada] Código de error.</span><span class="sxs-lookup"><span data-stu-id="05b34-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="05b34-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05b34-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="05b34-110">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="05b34-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="05b34-111">Esto debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="05b34-111">This must be 0.</span></span> 
    
 <span data-ttu-id="05b34-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="05b34-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="05b34-113">[out] Puntero a la estructura **MAPIERROR** que contiene la información extendida para el error.</span><span class="sxs-lookup"><span data-stu-id="05b34-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="05b34-114">Vea mapidefs.h para la definición de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="05b34-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="05b34-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="05b34-115">See also</span></span>



[<span data-ttu-id="05b34-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="05b34-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="05b34-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="05b34-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

