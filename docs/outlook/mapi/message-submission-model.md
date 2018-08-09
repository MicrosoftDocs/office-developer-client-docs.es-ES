---
title: Modelo de envío de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818408"
---
# <a name="message-submission-model"></a><span data-ttu-id="05171-103">Modelo de envío de mensajes</span><span class="sxs-lookup"><span data-stu-id="05171-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="05171-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05171-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05171-105">Envío de mensajes se realiza mediante una serie de llamadas desde la cola de MAPI para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="05171-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="05171-106">Las llamadas se ordenan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="05171-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="05171-107">La cola MAPI llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), pasando un [IMessage: IMAPIProp](imessageimapiprop.md) una instancia para comenzar el proceso.</span><span class="sxs-lookup"><span data-stu-id="05171-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="05171-108">El proveedor de transporte, a continuación, coloca un valor de referencia: un identificador definido por el transporte en futuro usa referencias a este mensaje, en la ubicación que se hace referencia en **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="05171-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="05171-109">El proveedor de transporte tiene acceso a los datos del mensaje mediante el uso de la instancia que se pase **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="05171-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="05171-110">Para cada destinatario en el pasado **IMessage** para la que acepta responsabilidad, el proveedor de transporte establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) y, a continuación, se devuelve.</span><span class="sxs-lookup"><span data-stu-id="05171-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="05171-111">El proveedor de transporte puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar si reconoce todos los destinatarios que no se puede entregar a, o para crear un informe de entrega estándar.</span><span class="sxs-lookup"><span data-stu-id="05171-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="05171-112">**StatusRecips** es una comodidad para los proveedores de transporte que ha determinado que algunos de los destinatarios no se puede entregar a o que han recibido la información de entrega de su sistema de mensajería subyacente que es posible que la aplicación cliente o de usuario encontrar útil.</span><span class="sxs-lookup"><span data-stu-id="05171-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="05171-113">Llamada de la cola MAPI a [IXPLogon::EndMessage](ixplogon-endmessage.md) es la entregue responsabilidad final para el mensaje de la cola de MAPI para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="05171-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="05171-114">La cola MAPI puede usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar el mensaje de procesamiento durante las llamadas a **SubmitMessage** o **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="05171-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

