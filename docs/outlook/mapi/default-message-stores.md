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
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338048"
---
# <a name="default-message-stores"></a><span data-ttu-id="65c4d-103">Almacenes de mensajes predeterminados</span><span class="sxs-lookup"><span data-stu-id="65c4d-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="65c4d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65c4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65c4d-p101">Un almacén de mensajes predeterminado es aquel que las aplicaciones cliente pueden usar para las tareas generales de mensajería. Hay varias características opcionales para los proveedores de almacenes de mensajes que pasan a ser necesarios si el proveedor del almacén de mensajes va a usarse como almacén de mensajes predeterminado. Son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="65c4d-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="65c4d-108">Implementar las carpetas especiales: las carpetas Bandeja de entrada, Bandeja de salida y resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="65c4d-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="65c4d-109">Proporcionar informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="65c4d-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="65c4d-110">Permitir envíos de mensajes entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="65c4d-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="65c4d-111">Permitir la creación de mensajes con clases de mensaje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="65c4d-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="65c4d-112">Compatibilidad con las propiedades con nombre y varios valores.</span><span class="sxs-lookup"><span data-stu-id="65c4d-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="65c4d-113">Compatibilidad con el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), incluso si el proveedor del almacén de mensajes está estrechamente acoplado a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="65c4d-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="65c4d-p102">Compatibilidad con tablas de contenido asociadas. Para obtener más información, vea [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="65c4d-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="65c4d-116">Compatibilidad con la notificación de la cola MAPI cuando hay mensajes en la cola de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="65c4d-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65c4d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="65c4d-117">See also</span></span>



[<span data-ttu-id="65c4d-118">Desarrollar un proveedor de almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="65c4d-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

