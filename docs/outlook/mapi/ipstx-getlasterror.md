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
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414980"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="543d3-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="543d3-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="543d3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="543d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="543d3-105">Obtiene información extendida sobre el último error.</span><span class="sxs-lookup"><span data-stu-id="543d3-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="543d3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="543d3-106">Parameters</span></span>

 <span data-ttu-id="543d3-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="543d3-107">_hResult_</span></span>
  
>  <span data-ttu-id="543d3-108">a Código de error.</span><span class="sxs-lookup"><span data-stu-id="543d3-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="543d3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="543d3-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="543d3-110">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="543d3-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="543d3-111">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="543d3-111">This must be 0.</span></span> 
    
 <span data-ttu-id="543d3-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="543d3-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="543d3-113">contempla Puntero a la estructura **MAPIERROR** que contiene la información extendida del error.</span><span class="sxs-lookup"><span data-stu-id="543d3-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="543d3-114">Consulte mapidefs. h para obtener la definición de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="543d3-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="543d3-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="543d3-115">See also</span></span>



[<span data-ttu-id="543d3-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="543d3-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="543d3-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="543d3-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

