---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818009"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="8e9fe-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="8e9fe-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="8e9fe-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e9fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e9fe-105">Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="8e9fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e9fe-106">Parameters</span></span>

 <span data-ttu-id="8e9fe-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="8e9fe-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="8e9fe-108">[out] Un valor que indica la existencia de mensajes de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="8e9fe-109">Un valor distinto de cero indica que no hay mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e9fe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e9fe-110">Return value</span></span>

<span data-ttu-id="8e9fe-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e9fe-111">S_OK</span></span> 
  
> <span data-ttu-id="8e9fe-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e9fe-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e9fe-113">Remarks</span></span>

<span data-ttu-id="8e9fe-114">La cola MAPI llama periódicamente al método de **IXPLogon::Poll** si el proveedor de transporte indica que se debe sondear para nuevos mensajes, que el proveedor pasando el LOGON_SP_POLL marcar a la llamada a la [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) método al principio de una sesión.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="8e9fe-115">Si el proveedor de transporte que se indica en respuesta a la llamada de **sondeo** que hay uno o más mensajes de entrada disponibles para él al proceso, la cola MAPI llama al método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que al proveedor de proceso de la primera entrada Mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="8e9fe-116">El proveedor de transporte indica mensajes entrantes estableciendo el valor en el parámetro _lpulIncoming_ en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8e9fe-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e9fe-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e9fe-117">See also</span></span>



[<span data-ttu-id="8e9fe-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="8e9fe-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="8e9fe-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="8e9fe-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="8e9fe-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e9fe-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

