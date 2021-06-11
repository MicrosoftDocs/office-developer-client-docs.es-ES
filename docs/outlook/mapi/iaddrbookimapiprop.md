---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429827"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="4a429-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4a429-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="4a429-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a429-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a429-105">Admite el acceso a la libreta de direcciones MAPI e incluye operaciones como mostrar cuadros de diálogo comunes; abrir contenedores, usuarios de mensajería y listas de distribución; y realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="4a429-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a429-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4a429-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a429-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="4a429-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4a429-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="4a429-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4a429-109">Objetos de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="4a429-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="4a429-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4a429-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a429-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a429-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a429-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4a429-112">Called by:</span></span>  <br/> |<span data-ttu-id="4a429-113">Aplicaciones cliente, proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4a429-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="4a429-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="4a429-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a429-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="4a429-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="4a429-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="4a429-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4a429-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="4a429-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="4a429-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="4a429-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="4a429-119">No se puede escribir</span><span class="sxs-lookup"><span data-stu-id="4a429-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a429-120">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="4a429-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4a429-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4a429-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="4a429-122">Abre una entrada de libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="4a429-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="4a429-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4a429-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="4a429-124">Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones determinado para determinar si hacen referencia al mismo objeto de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4a429-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="4a429-125">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="4a429-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="4a429-126">Registra un cliente o proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4a429-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="4a429-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="4a429-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="4a429-128">Cancela un registro de notificación establecido anteriormente para una entrada de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4a429-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="4a429-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="4a429-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="4a429-130">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="4a429-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="4a429-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="4a429-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="4a429-132">Agrega un nuevo destinatario a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="4a429-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="4a429-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="4a429-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="4a429-134">Realiza la resolución de nombres, asignando identificadores de entrada a los destinatarios de una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4a429-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="4a429-135">Address</span><span class="sxs-lookup"><span data-stu-id="4a429-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="4a429-136">Muestra el Outlook de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4a429-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="4a429-137">Detalles</span><span class="sxs-lookup"><span data-stu-id="4a429-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="4a429-138">Muestra un cuadro de diálogo que muestra detalles sobre una entrada de libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="4a429-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="4a429-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="4a429-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="4a429-140">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="4a429-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="4a429-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="4a429-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="4a429-142">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="4a429-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="4a429-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="4a429-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="4a429-144">Devuelve el identificador de entrada del contenedor designado como libreta de direcciones personal (PAB).</span><span class="sxs-lookup"><span data-stu-id="4a429-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="4a429-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="4a429-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="4a429-146">Designa un contenedor concreto como la libreta de direcciones personal (PAB).</span><span class="sxs-lookup"><span data-stu-id="4a429-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="4a429-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="4a429-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="4a429-148">Devuelve el identificador de entrada del contenedor de libreta de direcciones inicial.</span><span class="sxs-lookup"><span data-stu-id="4a429-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="4a429-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="4a429-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="4a429-150">Establece el contenedor especificado como el contenedor de libreta de direcciones predeterminado que está disponible inicialmente.</span><span class="sxs-lookup"><span data-stu-id="4a429-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="4a429-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4a429-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="4a429-152">Devuelve una lista ordenada de identificadores de entrada de los contenedores que se incluirán en el proceso de resolución de nombres iniciado por el [método ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="4a429-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="4a429-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4a429-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="4a429-154">Establece una nueva ruta de búsqueda en el perfil que se usa para el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="4a429-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="4a429-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="4a429-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="4a429-156">Prepara una lista de destinatarios para su uso posterior por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4a429-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a429-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a429-157">See also</span></span>



[<span data-ttu-id="4a429-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4a429-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

