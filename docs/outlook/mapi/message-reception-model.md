---
title: Modelo de recepción de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415120"
---
# <a name="message-reception-model"></a><span data-ttu-id="846e8-103">Modelo de recepción de mensajes</span><span class="sxs-lookup"><span data-stu-id="846e8-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="846e8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="846e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="846e8-105">El proveedor de transporte controla si la cola MAPI debe sondear el correo entrante o si realiza una llamada a la cola MAPI cuando llega el nuevo correo.</span><span class="sxs-lookup"><span data-stu-id="846e8-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="846e8-106">El proveedor de transporte establece la SP_LOGON_POLL cuando devuelve desde [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar sondeo.</span><span class="sxs-lookup"><span data-stu-id="846e8-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="846e8-107">De lo contrario, el proveedor de transporte [usa IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible.</span><span class="sxs-lookup"><span data-stu-id="846e8-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="846e8-108">Después de saber que el correo entrante está disponible, la cola MAPI abre un nuevo mensaje y pide al proveedor de transporte que almacene las propiedades del mensaje recibido en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="846e8-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="846e8-109">Este proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="846e8-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="846e8-110">Los mensajes disponibles se indican mediante el proveedor de transporte que llama **a IMAPISupport::SpoolerNotify** o mediante la cola MAPI que llama [a IXPLogon::P oll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="846e8-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="846e8-111">La cola MAPI llama a [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="846e8-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="846e8-112">El proveedor de transporte coloca un valor de referencia en la ubicación a la que se hace referencia **en StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="846e8-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="846e8-113">Estos valores de referencia permiten que el proveedor de transporte y la cola MAPI realicen un seguimiento del mensaje que se está procesando cuando hay varios mensajes que entregar.</span><span class="sxs-lookup"><span data-stu-id="846e8-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="846e8-114">El proveedor de transporte almacena los datos del mensaje en la [instancia IMessage : IMAPIProp pasada.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="846e8-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="846e8-115">El proveedor de transporte llama al [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) en la **instancia de IMessage** y devuelve desde **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="846e8-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="846e8-116">La cola MAPI llama a [IXPLogon::TransportNotify si](ixplogon-transportnotify.md) debe detener la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="846e8-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="846e8-117">Si un proveedor de transporte debe entregar un gran número de mensajes y el proveedor de transporte usa **IMAPISupport::SpoolerNotify** en lugar de **IXPLogon::P oll**, debe tenerse cuidado de no llamar a **SpoolerNotify** con demasiada frecuencia para no quitar tiempo de CPU a otros proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="846e8-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="846e8-118">La cola MAPI tiene lógica para evitar que esto ocurra, pero, en general, el intervalo entre las llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte en procesar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="846e8-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="846e8-119">>, es posible que la cola MAPI no procese un mensaje entrante inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="846e8-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="846e8-120">La cola MAPI puede pedir al proveedor de transporte que realice otras tareas antes de recibir el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="846e8-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

