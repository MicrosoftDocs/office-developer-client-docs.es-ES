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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431704"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="a333a-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a333a-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="a333a-104">Obtiene una cadena de mensaje para el error especificado.</span><span class="sxs-lookup"><span data-stu-id="a333a-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a333a-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a333a-105">Quick info</span></span>

<span data-ttu-id="a333a-106">Consulte [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a333a-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="a333a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a333a-107">Parameters</span></span>

<span data-ttu-id="a333a-108">_Departamento_</span><span class="sxs-lookup"><span data-stu-id="a333a-108">_hr_</span></span>
  
> <span data-ttu-id="a333a-109">a Código de error que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a333a-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="a333a-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="a333a-110">_ppwszError_</span></span>
  
> <span data-ttu-id="a333a-111">contempla Mensaje de error que corresponde a *HR* .</span><span class="sxs-lookup"><span data-stu-id="a333a-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a333a-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a333a-112">Return values</span></span>

|<span data-ttu-id="a333a-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="a333a-113">**HRESULT**</span></span>|<span data-ttu-id="a333a-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="a333a-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a333a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a333a-115">S_OK</span></span>  <br/> |<span data-ttu-id="a333a-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="a333a-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a333a-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a333a-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a333a-118">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a333a-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a333a-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="a333a-119">See also</span></span>

- [<span data-ttu-id="a333a-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="a333a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

