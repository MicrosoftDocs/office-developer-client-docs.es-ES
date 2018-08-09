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
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817104"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="1aaa7-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="1aaa7-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="1aaa7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1aaa7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1aaa7-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1aaa7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1aaa7-106">Parameters</span></span>

 <span data-ttu-id="1aaa7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1aaa7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1aaa7-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1aaa7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aaa7-109">Return value</span></span>

<span data-ttu-id="1aaa7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1aaa7-110">S_OK</span></span> 
  
> <span data-ttu-id="1aaa7-111">El proceso de cierre de sesión iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aaa7-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1aaa7-112">Remarks</span></span>

<span data-ttu-id="1aaa7-113">Normalmente, se inicia el proceso de cierre de sesión cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="1aaa7-114">MAPI, a continuación, llama al método **IABLogon::Logoff** de cada proveedor de la libreta de direcciones para iniciar el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="1aaa7-115">El método **IABLogon::Logoff** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1aaa7-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="1aaa7-116">Libera todos los objetos abiertos, como los objetos secundarios o el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="1aaa7-117">Libera el objeto de Ayuda del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1aaa7-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="1aaa7-118">Para obtener más información acerca del proceso de cierre de sesión de los proveedores de la libreta de direcciones, vea [Cerrando hacia abajo un proveedor de servicios](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1aaa7-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1aaa7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aaa7-119">See also</span></span>



[<span data-ttu-id="1aaa7-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1aaa7-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="1aaa7-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1aaa7-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

