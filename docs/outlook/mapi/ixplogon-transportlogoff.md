---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351586"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="5f604-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="5f604-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="5f604-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f604-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f604-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="5f604-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5f604-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f604-106">Parameters</span></span>

 <span data-ttu-id="5f604-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f604-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5f604-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f604-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f604-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f604-109">Return value</span></span>

<span data-ttu-id="5f604-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f604-110">S_OK</span></span> 
  
> <span data-ttu-id="5f604-111">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="5f604-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="5f604-112">Si se devuelve un valor que no sea S_OK, se cierra la sesión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5f604-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f604-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f604-113">Remarks</span></span>

<span data-ttu-id="5f604-114">La cola MAPI llama al método **IXPLogon:: TransportLogoff** para terminar una sesión de proveedor de transporte para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="5f604-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="5f604-115">Antes de llamar a **TransportLogoff**, la cola MAPI descarta los datos sobre los tipos de direcciones de mensajería admitidos para esta sesión pasados en el método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="5f604-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5f604-116">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="5f604-116">Notes to implementers</span></span>

<span data-ttu-id="5f604-117">El proveedor de transporte debe estar preparado para aceptar una llamada a **TransportLogoff** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="5f604-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="5f604-118">Si un mensaje está en curso, el proveedor debe detener el proceso de envío.</span><span class="sxs-lookup"><span data-stu-id="5f604-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="5f604-119">El proveedor de transporte debe liberar todos los recursos asignados a su sesión actual.</span><span class="sxs-lookup"><span data-stu-id="5f604-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="5f604-120">Si ha asignado memoria para esta sesión con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , debe liberar la memoria mediante la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5f604-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="5f604-121">Cualquier memoria asignada por el proveedor de transporte para atender las llamadas al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) se puede publicar de forma segura en este momento.</span><span class="sxs-lookup"><span data-stu-id="5f604-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="5f604-122">Normalmente, al completar una llamada **TransportLogoff** , un proveedor primero debe invalidar su objeto de inicio de sesión llamando al método [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) y, a continuación, liberando su objeto de soporte.</span><span class="sxs-lookup"><span data-stu-id="5f604-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="5f604-123">La implementación del proveedor de **TransportLogoff** debe liberar el objeto de soporte por última vez, ya que, cuando se libera el objeto de compatibilidad, la cola MAPI también puede liberar el propio objeto proveedor.</span><span class="sxs-lookup"><span data-stu-id="5f604-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f604-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f604-124">See also</span></span>



[<span data-ttu-id="5f604-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="5f604-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="5f604-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="5f604-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="5f604-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="5f604-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="5f604-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5f604-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5f604-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5f604-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5f604-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f604-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

