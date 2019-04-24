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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339301"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="c5a5f-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="c5a5f-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="c5a5f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5a5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5a5f-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c5a5f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c5a5f-106">Parameters</span></span>

 <span data-ttu-id="c5a5f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5a5f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c5a5f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5a5f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5a5f-109">Return value</span></span>

<span data-ttu-id="c5a5f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5a5f-110">S_OK</span></span> 
  
> <span data-ttu-id="c5a5f-111">El proceso de cierre de sesión se inició correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5a5f-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5a5f-112">Remarks</span></span>

<span data-ttu-id="c5a5f-113">Normalmente, el proceso de cierre de sesión se inicia cuando un cliente llama al método [IMAPISession:: Logoff](imapisession-logoff.md) para finalizar una sesión.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="c5a5f-114">MAPI, a continuación, llama al método **IABLogon:: Logoff** del proveedor de la libreta de direcciones para iniciar el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="c5a5f-115">El método **IABLogon:: Logoff** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5a5f-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="c5a5f-116">Libera todos los objetos abiertos, por ejemplo, los subobjetos o el objeto status.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="c5a5f-117">Libera el objeto de compatibilidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c5a5f-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="c5a5f-118">Para obtener más información acerca del proceso de cierre de sesión de los proveedores de la libreta de direcciones, consulte [apagar un proveedor de servicios](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c5a5f-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5a5f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5a5f-119">See also</span></span>



[<span data-ttu-id="c5a5f-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c5a5f-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="c5a5f-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5a5f-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

