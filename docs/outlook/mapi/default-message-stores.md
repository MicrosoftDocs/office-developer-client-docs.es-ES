---
title: Almacenes de mensajes predeterminados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576914"
---
# <a name="default-message-stores"></a><span data-ttu-id="863d2-103">Almacenes de mensajes predeterminados</span><span class="sxs-lookup"><span data-stu-id="863d2-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="863d2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="863d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="863d2-p101">Un almacén de mensajes predeterminado es aquel que las aplicaciones cliente pueden usar para las tareas generales de mensajería. Hay varias características opcionales para los proveedores de almacenes de mensajes que pasan a ser necesarios si el proveedor del almacén de mensajes va a usarse como almacén de mensajes predeterminado. Son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="863d2-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="863d2-108">Implementar las carpetas especiales: las carpetas Bandeja de entrada, Bandeja de salida y resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="863d2-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="863d2-109">Proporcionar informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="863d2-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="863d2-110">Permitir envíos de mensajes entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="863d2-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="863d2-111">Permitir la creación de mensajes con clases de mensaje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="863d2-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="863d2-112">Compatibilidad con las propiedades con nombre y varios valores.</span><span class="sxs-lookup"><span data-stu-id="863d2-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="863d2-113">Compatibilidad con el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), incluso si el proveedor del almacén de mensajes está estrechamente acoplado a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="863d2-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="863d2-p102">Compatibilidad con tablas de contenido asociadas. Para obtener más información, vea [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="863d2-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="863d2-116">Compatibilidad con la notificación de la cola MAPI cuando hay mensajes en la cola de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="863d2-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="863d2-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="863d2-117">See also</span></span>



[<span data-ttu-id="863d2-118">Desarrollar un proveedor de almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="863d2-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

