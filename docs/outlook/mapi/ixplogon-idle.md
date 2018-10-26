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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578019"
---
# <a name="ixplogonidle"></a><span data-ttu-id="cd91a-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="cd91a-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="cd91a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd91a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd91a-105">Indica que el sistema está inactivo, habilitar el proveedor de transporte realizar operaciones de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="cd91a-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cd91a-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="cd91a-106">Parameters</span></span>

 <span data-ttu-id="cd91a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd91a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cd91a-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cd91a-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cd91a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd91a-109">Return value</span></span>

<span data-ttu-id="cd91a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd91a-110">S_OK</span></span> 
  
> <span data-ttu-id="cd91a-111">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="cd91a-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd91a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd91a-112">Remarks</span></span>

<span data-ttu-id="cd91a-113">La cola MAPI llama periódicamente el método **IXPLogon::Idle** , si solicitado durante las horas de cuando el sistema está inactivo, se pasa el indicador XP_LOGON_SP en la llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) que abrió la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="cd91a-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="cd91a-114">A veces cuando el sistema está inactivo, el proveedor de transporte puede realizar operaciones en segundo plano que no son adecuados durante el resto de las llamadas a o de que se producen de forma regular.</span><span class="sxs-lookup"><span data-stu-id="cd91a-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd91a-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd91a-115">See also</span></span>



[<span data-ttu-id="cd91a-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="cd91a-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="cd91a-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd91a-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

