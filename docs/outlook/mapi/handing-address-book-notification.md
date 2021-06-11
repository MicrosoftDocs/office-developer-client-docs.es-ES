---
title: Administrar las notificaciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413538"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="22f3f-103">Administrar las notificaciones de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="22f3f-103">Handing address book notification</span></span>
  
<span data-ttu-id="22f3f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22f3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22f3f-105">Las notificaciones de libreta de direcciones permiten a un cliente conocer los eventos que se producen en cualquier entrada de la libreta de direcciones o en una entrada determinada.</span><span class="sxs-lookup"><span data-stu-id="22f3f-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="22f3f-106">Puede registrarse para estas notificaciones a través de la libreta de direcciones MAPI llamando a [IAddrBook::Advise](iaddrbook-advise.md) o a través de la jerarquía o la tabla de contenido de un contenedor de libreta de direcciones llamando a [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="22f3f-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="22f3f-107">Especifique el identificador de entrada de un contenedor de libreta de direcciones, una lista de distribución o un usuario de mensajería si está registrando notificaciones en una entrada determinada y NULL si se registra para notificaciones en toda la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="22f3f-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="22f3f-108">El identificador de entrada debe representar un usuario de mensajería o una lista de distribución en un contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="22f3f-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="22f3f-109">**IAddrBook::Advise** examina este identificador de entrada para determinar qué proveedor de libreta de direcciones es responsable del objeto correspondiente y reenvía la llamada al método [IABLogon::Advise](iablogon-advise.md) del proveedor de libreta de direcciones correspondiente.</span><span class="sxs-lookup"><span data-stu-id="22f3f-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="22f3f-110">Los clientes pueden registrarse para los siguientes tipos de eventos en las entradas de la libreta de direcciones:</span><span class="sxs-lookup"><span data-stu-id="22f3f-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="22f3f-111">Error crítico</span><span class="sxs-lookup"><span data-stu-id="22f3f-111">Critical error</span></span>
    
- <span data-ttu-id="22f3f-112">Cualquiera de los eventos de objeto (creados, modificados, eliminados, movidos o copiados)</span><span class="sxs-lookup"><span data-stu-id="22f3f-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="22f3f-113">Tabla modificada</span><span class="sxs-lookup"><span data-stu-id="22f3f-113">Table modified</span></span>
    
<span data-ttu-id="22f3f-114">Normalmente, el registro solo se produce en el contenido del contenedor de libreta de direcciones y en las tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="22f3f-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="22f3f-115">Es raro que los clientes se registren con los objetos de lista de distribución y usuario de mensajería de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="22f3f-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="22f3f-116">Esto se debe a:</span><span class="sxs-lookup"><span data-stu-id="22f3f-116">This is because:</span></span>
  
- <span data-ttu-id="22f3f-117">Muchos proveedores de libreta de direcciones no admiten notificaciones en sus listas de distribución y usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="22f3f-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="22f3f-118">Las notificaciones de tabla son suficientes para realizar un seguimiento de los cambios y notificarlos a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="22f3f-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

