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
ms.openlocfilehash: a20fdd45c39cc2147f8fdc7b1998ff6d1b0797bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586210"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="b357e-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="b357e-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="b357e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b357e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b357e-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="b357e-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b357e-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b357e-106">Parameters</span></span>

 <span data-ttu-id="b357e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b357e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b357e-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b357e-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b357e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b357e-109">Return value</span></span>

<span data-ttu-id="b357e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b357e-110">S_OK</span></span> 
  
> <span data-ttu-id="b357e-111">El proceso de cierre de sesión iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b357e-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b357e-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b357e-112">Remarks</span></span>

<span data-ttu-id="b357e-113">Normalmente, se inicia el proceso de cierre de sesión cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión.</span><span class="sxs-lookup"><span data-stu-id="b357e-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="b357e-114">MAPI, a continuación, llama al método **IABLogon::Logoff** de cada proveedor de la libreta de direcciones para iniciar el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="b357e-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="b357e-115">El método **IABLogon::Logoff** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b357e-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="b357e-116">Libera todos los objetos abiertos, como los objetos secundarios o el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="b357e-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="b357e-117">Libera el objeto de Ayuda del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b357e-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="b357e-118">Para obtener más información acerca del proceso de cierre de sesión de los proveedores de la libreta de direcciones, vea [Cerrando hacia abajo un proveedor de servicios](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b357e-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b357e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b357e-119">See also</span></span>



[<span data-ttu-id="b357e-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="b357e-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="b357e-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b357e-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

