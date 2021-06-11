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
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421126"
---
# <a name="message-submission-model"></a><span data-ttu-id="21204-103">Modelo de envío de mensajes</span><span class="sxs-lookup"><span data-stu-id="21204-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="21204-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21204-105">El envío de mensajes se realiza mediante una serie de llamadas desde la cola MAPI al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="21204-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="21204-106">Las llamadas se secuencian de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="21204-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="21204-107">La cola MAPI llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), pasando una [instancia de IMessage : IMAPIProp,](imessageimapiprop.md) para iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="21204-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="21204-108">A continuación, el proveedor de transporte coloca un valor de referencia , un identificador definido por el transporte usado en referencias futuras a este mensaje, en la ubicación a la que se hace referencia en **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="21204-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="21204-109">El proveedor de transporte tiene acceso a los datos del mensaje mediante la instancia **IMessage** pasada.</span><span class="sxs-lookup"><span data-stu-id="21204-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="21204-110">Para cada destinatario del **IMessage** pasado del que acepta responsabilidad, el proveedor de transporte establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) y, a continuación, devuelve.</span><span class="sxs-lookup"><span data-stu-id="21204-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="21204-111">El proveedor de transporte puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar si reconoce a los destinatarios a los que no se puede entregar o para crear un informe de entrega estándar.</span><span class="sxs-lookup"><span data-stu-id="21204-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="21204-112">**StatusRecips** es una comodidad para los proveedores de transporte que han determinado que algunos de los destinatarios no se pueden entregar o que han recibido información de entrega de su sistema de mensajería subyacente que el usuario o la aplicación cliente podrían resultar útiles.</span><span class="sxs-lookup"><span data-stu-id="21204-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="21204-113">La llamada de la cola MAPI a [IXPLogon::EndMessage](ixplogon-endmessage.md) es la entrega de responsabilidad final del mensaje de la cola MAPI al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="21204-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="21204-114">La cola MAPI puede usar [IXPLogon::TransportNotify para](ixplogon-transportnotify.md) cancelar el procesamiento de mensajes durante las llamadas **SubmitMessage** o **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="21204-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

