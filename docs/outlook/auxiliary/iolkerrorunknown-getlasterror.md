---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtiene una cadena de mensaje para el error especificado.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816251"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="dc593-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dc593-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="dc593-104">Obtiene una cadena de mensaje para el error especificado.</span><span class="sxs-lookup"><span data-stu-id="dc593-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="dc593-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="dc593-105">Quick info</span></span>

<span data-ttu-id="dc593-106">Vea [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="dc593-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="dc593-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc593-107">Parameters</span></span>

<span data-ttu-id="dc593-108">_recursos humanos_</span><span class="sxs-lookup"><span data-stu-id="dc593-108">_hr_</span></span>
  
> <span data-ttu-id="dc593-109">[entrada] Código de error que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="dc593-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="dc593-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="dc593-110">_ppwszError_</span></span>
  
> <span data-ttu-id="dc593-111">[out] El mensaje de error que corresponde a *recursos humanos* .</span><span class="sxs-lookup"><span data-stu-id="dc593-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="dc593-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dc593-112">Return values</span></span>

|<span data-ttu-id="dc593-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="dc593-113">**HRESULT**</span></span>|<span data-ttu-id="dc593-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc593-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc593-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc593-115">S_OK</span></span>  <br/> |<span data-ttu-id="dc593-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="dc593-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="dc593-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dc593-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dc593-118">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="dc593-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc593-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc593-119">See also</span></span>

- [<span data-ttu-id="dc593-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="dc593-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

