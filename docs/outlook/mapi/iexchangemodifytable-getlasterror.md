---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594295"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="00d4d-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="00d4d-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="00d4d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00d4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00d4d-105">Devuelve información sobre el último error que se produjo en un objeto table.</span><span class="sxs-lookup"><span data-stu-id="00d4d-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="00d4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00d4d-106">Parameters</span></span>

 <span data-ttu-id="00d4d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="00d4d-107">_hResult_</span></span>
  
> <span data-ttu-id="00d4d-108">[entrada] El valor devuelto por el método fallidas.</span><span class="sxs-lookup"><span data-stu-id="00d4d-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="00d4d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00d4d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="00d4d-110">[entrada] No se usa, se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="00d4d-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="00d4d-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="00d4d-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="00d4d-112">[out] Apunta a una estructura MAPI [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para un objeto table.</span><span class="sxs-lookup"><span data-stu-id="00d4d-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="00d4d-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="00d4d-113">See also</span></span>



[<span data-ttu-id="00d4d-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00d4d-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="00d4d-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="00d4d-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="00d4d-116">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="00d4d-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

