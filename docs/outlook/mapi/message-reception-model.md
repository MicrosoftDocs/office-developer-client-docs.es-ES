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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356948"
---
# <a name="message-reception-model"></a><span data-ttu-id="6f821-103">Modelo de recepción de mensajes</span><span class="sxs-lookup"><span data-stu-id="6f821-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="6f821-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f821-105">El proveedor de transporte controla si la cola MAPI debe sondearla para el correo entrante o si realiza una devolución de llamada a la cola MAPI cuando llega correo nuevo.</span><span class="sxs-lookup"><span data-stu-id="6f821-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="6f821-106">El proveedor de transporte establece la marca SP_LOGON_POLL cuando vuelve de [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para solicitar el sondeo.</span><span class="sxs-lookup"><span data-stu-id="6f821-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="6f821-107">De lo contrario, el proveedor de transporte usa [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible.</span><span class="sxs-lookup"><span data-stu-id="6f821-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="6f821-108">Una vez que se ha familiarizado con el correo entrante disponible, la cola MAPI abre un nuevo mensaje y pide al proveedor de transporte que almacene las propiedades del mensaje recibido en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6f821-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="6f821-109">Este proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6f821-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="6f821-110">Los mensajes disponibles los indica el proveedor de transporte que llama a **IMAPISupport:: SpoolerNotify** o por el administrador de trabajos en cola MAPI llamando a [IXPLogon::P Oll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="6f821-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="6f821-111">La cola MAPI llama a [IXPLogon:: StartMessage](ixplogon-startmessage.md) para iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="6f821-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="6f821-112">El proveedor de transporte coloca un valor de referencia en la ubicación a la que se hace referencia en **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="6f821-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="6f821-113">Estos valores de referencia permiten al proveedor de transporte y a la cola MAPI realizar un seguimiento del mensaje que se está procesando cuando hay varios mensajes que entregar.</span><span class="sxs-lookup"><span data-stu-id="6f821-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="6f821-114">El proveedor de transporte almacena los datos del mensaje en la instancia de [IMessage: IMAPIProp](imessageimapiprop.md) pasada.</span><span class="sxs-lookup"><span data-stu-id="6f821-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="6f821-115">El proveedor de transporte llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en la instancia **IMessage** y vuelve de **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="6f821-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="6f821-116">La cola MAPI llama a [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) si debe detener la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6f821-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6f821-117">Si un proveedor de transporte debe entregar un gran número de mensajes y el proveedor de transporte usa **IMAPISupport:: SpoolerNotify** en lugar de **IXPLogon::P Oll**, debe tenerse cuidado de no llamar a **SpoolerNotify** con demasiada frecuencia para privar a otros proveedores de transporte de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="6f821-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="6f821-118">La cola MAPI tiene lógica para evitar que esto suceda, pero, en general, el intervalo entre llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte en procesar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6f821-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="6f821-119">> también puede que la cola MAPI no procese un mensaje entrante inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6f821-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="6f821-120">La cola MAPI puede pedir al proveedor de transporte que realice otras tareas antes de recibir el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="6f821-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

