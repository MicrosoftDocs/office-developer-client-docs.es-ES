---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416401"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="d2329-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="d2329-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="d2329-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2329-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2329-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="d2329-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d2329-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2329-106">Parameters</span></span>

 <span data-ttu-id="d2329-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2329-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d2329-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d2329-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2329-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2329-109">Return value</span></span>

<span data-ttu-id="d2329-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2329-110">S_OK</span></span> 
  
> <span data-ttu-id="d2329-111">El proceso de cierre de sesión se inició correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2329-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2329-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2329-112">Remarks</span></span>

<span data-ttu-id="d2329-113">El proceso de cierre de sesión normalmente se inicia cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión.</span><span class="sxs-lookup"><span data-stu-id="d2329-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="d2329-114">A continuación, MAPI llama al método **IABLogon::Logoff** de cada proveedor de libreta de direcciones para iniciar el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="d2329-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="d2329-115">El **método IABLogon::Logoff** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2329-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="d2329-116">Libera todos los objetos abiertos, como cualquier subobjeto o el objeto status.</span><span class="sxs-lookup"><span data-stu-id="d2329-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="d2329-117">Libera el objeto de soporte técnico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d2329-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="d2329-118">Para obtener más información sobre el proceso de cierre de sesión de los proveedores de libreta de direcciones, vea [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d2329-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2329-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2329-119">See also</span></span>



[<span data-ttu-id="d2329-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d2329-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d2329-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2329-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

