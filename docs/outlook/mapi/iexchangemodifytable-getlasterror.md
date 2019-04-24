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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350865"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="3be53-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3be53-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="3be53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3be53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3be53-105">Devuelve información sobre el último error que se produjo en un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="3be53-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="3be53-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3be53-106">Parameters</span></span>

 <span data-ttu-id="3be53-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="3be53-107">_hResult_</span></span>
  
> <span data-ttu-id="3be53-108">a Valor devuelto del método que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="3be53-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="3be53-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3be53-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3be53-110">a No se usa, se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3be53-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="3be53-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3be53-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3be53-112">contempla Apunta a una estructura [MAPIERROR](mapierror.md) de MAPI que contiene información sobre el último error que se produjo en un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="3be53-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3be53-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3be53-113">See also</span></span>



[<span data-ttu-id="3be53-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3be53-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="3be53-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3be53-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="3be53-116">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3be53-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

