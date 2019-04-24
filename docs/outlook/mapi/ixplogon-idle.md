---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298484"
---
# <a name="ixplogonidle"></a><span data-ttu-id="fd10f-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="fd10f-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="fd10f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd10f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd10f-105">Indica que el sistema está inactivo, lo que permite al proveedor de transporte realizar operaciones de baja prioridad.</span><span class="sxs-lookup"><span data-stu-id="fd10f-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fd10f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd10f-106">Parameters</span></span>

 <span data-ttu-id="fd10f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd10f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fd10f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fd10f-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd10f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd10f-109">Return value</span></span>

<span data-ttu-id="fd10f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd10f-110">S_OK</span></span> 
  
> <span data-ttu-id="fd10f-111">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="fd10f-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd10f-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd10f-112">Remarks</span></span>

<span data-ttu-id="fd10f-113">La cola MAPI llama periódicamente al método **IXPLogon:: idle** , si se le solicita, siempre que el sistema está inactivo pasando la marca XP_LOGON_SP en la llamada al método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) que abrió la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="fd10f-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="fd10f-114">En ocasiones, cuando el sistema está inactivo, el proveedor de transporte puede realizar operaciones en segundo plano que no son adecuadas durante otras llamadas, o que tienen que realizarse de forma regular.</span><span class="sxs-lookup"><span data-stu-id="fd10f-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd10f-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd10f-115">See also</span></span>



[<span data-ttu-id="fd10f-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="fd10f-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="fd10f-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd10f-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

