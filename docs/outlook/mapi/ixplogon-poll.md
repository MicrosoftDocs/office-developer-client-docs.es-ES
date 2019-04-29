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
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425277"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="1cadd-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="1cadd-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="1cadd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cadd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cadd-105">Indica si el proveedor de transporte ha recibido uno o más mensajes de entrada.</span><span class="sxs-lookup"><span data-stu-id="1cadd-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="1cadd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1cadd-106">Parameters</span></span>

 <span data-ttu-id="1cadd-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="1cadd-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="1cadd-108">contempla Un valor que indica la existencia de mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1cadd-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="1cadd-109">Un valor distinto de cero indica que hay mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1cadd-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cadd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cadd-110">Return value</span></span>

<span data-ttu-id="1cadd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cadd-111">S_OK</span></span> 
  
> <span data-ttu-id="1cadd-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1cadd-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cadd-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1cadd-113">Remarks</span></span>

<span data-ttu-id="1cadd-114">La cola MAPI llama periódicamente al método **IXPLogon::P Oll** si el proveedor de transporte indica que debe realizarse un sondeo de los nuevos mensajes, que el proveedor realiza pasando la marca LOGON_SP_POLL a la llamada a [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) al principio de una sesión.</span><span class="sxs-lookup"><span data-stu-id="1cadd-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="1cadd-115">Si el proveedor de transporte indica en respuesta a \*\*\*\* la llamada de sondeo que hay uno o más mensajes entrantes disponibles para que los procese, la cola MAPI llama al método [IXPLogon:: StartMessage](ixplogon-startmessage.md) para permitir que el proveedor procese el primer entrada mensaje.</span><span class="sxs-lookup"><span data-stu-id="1cadd-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="1cadd-116">El proveedor de transporte indica los mensajes entrantes estableciendo el valor del parámetro _lpulIncoming_ en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1cadd-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cadd-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="1cadd-117">See also</span></span>



[<span data-ttu-id="1cadd-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="1cadd-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="1cadd-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="1cadd-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="1cadd-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cadd-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

