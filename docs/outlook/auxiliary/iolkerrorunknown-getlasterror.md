---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtiene una cadena de mensaje para el error especificado.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321885"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="8cf57-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8cf57-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="8cf57-104">Obtiene una cadena de mensaje para el error especificado.</span><span class="sxs-lookup"><span data-stu-id="8cf57-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8cf57-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8cf57-105">Quick info</span></span>

<span data-ttu-id="8cf57-106">Consulte [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8cf57-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="8cf57-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8cf57-107">Parameters</span></span>

<span data-ttu-id="8cf57-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="8cf57-108">_hr_</span></span>
  
> <span data-ttu-id="8cf57-109">a Código de error que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="8cf57-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="8cf57-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="8cf57-110">_ppwszError_</span></span>
  
> <span data-ttu-id="8cf57-111">contempla Mensaje de error que corresponde a *HR* .</span><span class="sxs-lookup"><span data-stu-id="8cf57-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8cf57-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8cf57-112">Return values</span></span>

|<span data-ttu-id="8cf57-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8cf57-113">**HRESULT**</span></span>|<span data-ttu-id="8cf57-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cf57-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cf57-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cf57-115">S_OK</span></span>  <br/> |<span data-ttu-id="8cf57-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="8cf57-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8cf57-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cf57-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cf57-118">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8cf57-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cf57-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cf57-119">See also</span></span>

- [<span data-ttu-id="8cf57-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="8cf57-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

