---
title: Entrega de notificación de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816922"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="961f0-103">Entrega de notificación de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="961f0-103">Handing address book notification</span></span>
  
<span data-ttu-id="961f0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="961f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="961f0-105">Las notificaciones de la libreta de direcciones, permitir que un cliente obtener más información de eventos que se producen en cualquier entrada de la libreta de direcciones o en un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="961f0-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="961f0-106">Se pueden registrar para estas notificaciones a través de la libreta de direcciones MAPI mediante una llamada a [IAddrBook::Advise](iaddrbook-advise.md) o a través de la jerarquía de un contenedor de la libreta de direcciones o una tabla de contenido mediante una llamada a [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="961f0-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="961f0-107">Especifique el identificador de entrada de un contenedor de la libreta de direcciones, una lista de distribución o un usuario de mensajería si va a registrar para las notificaciones en una entrada en particular y NULL si se registra para las notificaciones en la libreta de direcciones completa.</span><span class="sxs-lookup"><span data-stu-id="961f0-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="961f0-108">El identificador de entrada debe representar un usuario de mensajería o lista de distribución en un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="961f0-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="961f0-109">**IAddrBook::Advise** examina este identificador de entrada para determinar qué dirección proveedor de libretas es responsable del objeto correspondiente y reenvía la llamada al método de [IABLogon::Advise](iablogon-advise.md) del proveedor de la libreta de dirección adecuada.</span><span class="sxs-lookup"><span data-stu-id="961f0-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="961f0-110">Los clientes pueden registrar para los siguientes tipos de eventos en las entradas de la libreta de direcciones:</span><span class="sxs-lookup"><span data-stu-id="961f0-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="961f0-111">Error crítico</span><span class="sxs-lookup"><span data-stu-id="961f0-111">Critical error</span></span>
    
- <span data-ttu-id="961f0-112">Cualquiera de los eventos del objeto (creado, modificado, eliminado, movido o copiado)</span><span class="sxs-lookup"><span data-stu-id="961f0-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="961f0-113">Tabla modificado</span><span class="sxs-lookup"><span data-stu-id="961f0-113">Table modified</span></span>
    
<span data-ttu-id="961f0-114">Normalmente, el registro se produce sólo en el contenido del contenedor de la libreta de direcciones y las tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="961f0-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="961f0-115">Es muy poco frecuente que los clientes registren con los objetos de lista de distribución y de usuario de mensajería de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="961f0-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="961f0-116">Esto es debido a que:</span><span class="sxs-lookup"><span data-stu-id="961f0-116">This is because:</span></span>
  
- <span data-ttu-id="961f0-117">Muchos de los proveedores de la libreta de direcciones no admiten notificaciones en sus listas de distribución y usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="961f0-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="961f0-118">Las notificaciones de tabla son suficientes para el seguimiento de los cambios e informando de ellos a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="961f0-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

