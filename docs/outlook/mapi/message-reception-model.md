---
title: Modelo de recepción de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818388"
---
# <a name="message-reception-model"></a><span data-ttu-id="ac969-103">Modelo de recepción de mensajes</span><span class="sxs-lookup"><span data-stu-id="ac969-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="ac969-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac969-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac969-105">El proveedor de transporte controla si la cola MAPI debe sondear de para el correo entrante o si realiza una devolución de llamada a la cola MAPI cuando llegue correo nuevo.</span><span class="sxs-lookup"><span data-stu-id="ac969-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="ac969-106">El proveedor de transporte establece la marca SP_LOGON_POLL cuando se devuelve desde [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar el sondeo.</span><span class="sxs-lookup"><span data-stu-id="ac969-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="ac969-107">De lo contrario, el proveedor de transporte usa [SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible.</span><span class="sxs-lookup"><span data-stu-id="ac969-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="ac969-108">Después de que el correo entrante está disponible de aprendizaje, la cola MAPI abre un nuevo mensaje y solicita el proveedor de transporte para almacenar las propiedades del mensaje recibido en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac969-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="ac969-109">Este proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ac969-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="ac969-110">Mensajes disponibles se indican por el proveedor de transporte de llamada **SpoolerNotify** o por la cola MAPI al llamar a [IXPLogon::Poll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="ac969-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="ac969-111">La cola MAPI llama a [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="ac969-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="ac969-112">El proveedor de transporte, coloca un valor de referencia en la ubicación que se hace referencia en **desea iniciar**.</span><span class="sxs-lookup"><span data-stu-id="ac969-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="ac969-113">Estos valores de referencia permitir que el proveedor de transporte y la cola de MAPI para realizar un seguimiento de mensaje que se está procesando cuando hay varios mensajes para entregar.</span><span class="sxs-lookup"><span data-stu-id="ac969-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="ac969-114">El proveedor de transporte almacena los datos del mensaje en el pasado [IMessage: IMAPIProp](imessageimapiprop.md) instancia.</span><span class="sxs-lookup"><span data-stu-id="ac969-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="ac969-115">El proveedor de transporte llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en la instancia de **IMessage** y se devuelve desde **desea iniciar**.</span><span class="sxs-lookup"><span data-stu-id="ac969-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="ac969-116">La cola MAPI llama a [IXPLogon::TransportNotify](ixplogon-transportnotify.md) si debe detener la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ac969-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ac969-117">Si un proveedor de transporte debe entregar a un gran número de mensajes y el proveedor de transporte está usando **SpoolerNotify** en lugar de **IXPLogon::Poll**, debe tener cuidado no para llamar a **SpoolerNotify** demasiado con frecuencia en orden para no PRIVARLE otros proveedores de transporte de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="ac969-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="ac969-118">La cola MAPI tienen lógica para evitar que esto ocurra, pero en general, el intervalo entre llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte para procesar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac969-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="ac969-119">> También, la cola MAPI no puede procesar un mensaje entrante inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ac969-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="ac969-120">La cola MAPI puede pedir el proveedor de transporte para llevar a cabo otras tareas antes de que recibe el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="ac969-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

