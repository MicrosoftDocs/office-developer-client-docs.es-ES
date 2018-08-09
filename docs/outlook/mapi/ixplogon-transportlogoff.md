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
ms.openlocfilehash: 195f2d718428eb8bb618fc982488c276d8a536da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818022"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="34b73-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="34b73-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="34b73-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34b73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34b73-105">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="34b73-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="34b73-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="34b73-106">Parameters</span></span>

 <span data-ttu-id="34b73-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34b73-107">_ulFlags_</span></span>
  
> <span data-ttu-id="34b73-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="34b73-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34b73-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34b73-109">Return value</span></span>

<span data-ttu-id="34b73-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="34b73-110">S_OK</span></span> 
  
> <span data-ttu-id="34b73-111">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="34b73-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="34b73-112">Si no se devuelve nada distinto de S_OK, el proveedor se cerró.</span><span class="sxs-lookup"><span data-stu-id="34b73-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34b73-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34b73-113">Remarks</span></span>

<span data-ttu-id="34b73-114">La cola MAPI llama al método de **IXPLogon::TransportLogoff** para finalizar una sesión de proveedor de transporte de un usuario concreto.</span><span class="sxs-lookup"><span data-stu-id="34b73-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="34b73-115">Antes de llamar a **TransportLogoff**, la cola MAPI descarta los datos acerca de los tipos de dirección de mensajería admitidos para esta sesión pasada en el método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="34b73-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34b73-116">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="34b73-116">Notes to implementers</span></span>

<span data-ttu-id="34b73-117">El proveedor de transporte debe estar preparado para aceptar una llamada a **TransportLogoff** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="34b73-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="34b73-118">Si un mensaje está en proceso, el proveedor debe detener el proceso de envío.</span><span class="sxs-lookup"><span data-stu-id="34b73-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="34b73-119">El proveedor de transporte debe liberar todos los recursos asignados para la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="34b73-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="34b73-120">Si ha asignado la memoria para esta sesión con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que debe liberar la memoria mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="34b73-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="34b73-121">Puede liberar memoria asignada por el proveedor de transporte para satisfacer las llamadas al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) sin ningún riesgo en este momento.</span><span class="sxs-lookup"><span data-stu-id="34b73-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="34b73-122">Normalmente, en completar una llamada **TransportLogoff** , un proveedor debe invalidar primero su objeto de inicio de sesión llamando al método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) y, a continuación, de su objeto de compatibilidad con la versión.</span><span class="sxs-lookup"><span data-stu-id="34b73-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="34b73-123">La implementación del proveedor de **TransportLogoff** debe liberar el objeto de soporte técnico por última vez, ya que cuando se libera el objeto de soporte, la cola MAPI también puede liberar el objeto de proveedor de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="34b73-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34b73-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="34b73-124">See also</span></span>



[<span data-ttu-id="34b73-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="34b73-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="34b73-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="34b73-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="34b73-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="34b73-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="34b73-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="34b73-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="34b73-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="34b73-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="34b73-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34b73-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

