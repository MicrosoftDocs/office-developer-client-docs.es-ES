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
ms.openlocfilehash: 0e39f2603a1eef45c456b7fb58744b79c6b75f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817138"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="8d4cb-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d4cb-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="8d4cb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d4cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d4cb-105">Admite el acceso a la libreta de direcciones MAPI e incluye operaciones como mostrar cuadros de diálogo comunes; contenedores de apertura, mensajería a los usuarios y las listas de distribución; y realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d4cb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d4cb-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="8d4cb-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="8d4cb-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8d4cb-109">Objetos de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="8d4cb-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="8d4cb-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d4cb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8d4cb-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="8d4cb-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-112">Called by:</span></span>  <br/> |<span data-ttu-id="8d4cb-113">Aplicaciones cliente, los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8d4cb-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="8d4cb-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8d4cb-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="8d4cb-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="8d4cb-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8d4cb-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="8d4cb-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="8d4cb-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="8d4cb-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="8d4cb-119">No se puede escribir</span><span class="sxs-lookup"><span data-stu-id="8d4cb-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8d4cb-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="8d4cb-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8d4cb-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8d4cb-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="8d4cb-122">Se abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8d4cb-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="8d4cb-124">Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones concreto para determinar si hacen referencia al mismo objeto de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-125">Aviso</span><span class="sxs-lookup"><span data-stu-id="8d4cb-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="8d4cb-126">Registra un proveedor de servicio o cliente para recibir notificaciones sobre los cambios realizados en una o más entradas en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-127">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="8d4cb-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="8d4cb-128">Cancela un registro de notificación establecido anteriormente para una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="8d4cb-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="8d4cb-130">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="8d4cb-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="8d4cb-132">Agrega a un nuevo destinatario a un contenedor de la libreta de direcciones o a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="8d4cb-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="8d4cb-134">Realiza la resolución de nombres, asignar los identificadores de entrada a los destinatarios en una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-135">Dirección</span><span class="sxs-lookup"><span data-stu-id="8d4cb-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="8d4cb-136">Muestra el cuadro de diálogo de la libreta de direcciones de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-137">Detalles</span><span class="sxs-lookup"><span data-stu-id="8d4cb-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="8d4cb-138">Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="8d4cb-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="8d4cb-140">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="8d4cb-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="8d4cb-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="8d4cb-142">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="8d4cb-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="8d4cb-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="8d4cb-144">Devuelve el identificador de entrada del contenedor que se designa como la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="8d4cb-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="8d4cb-146">Designa un contenedor determinado como la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="8d4cb-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="8d4cb-148">Devuelve el identificador de entrada para el contenedor de la libreta de direcciones inicial.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="8d4cb-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="8d4cb-150">Establece el contenedor especificado como el contenedor de libreta de direcciones predeterminada que inicialmente está disponible.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="8d4cb-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="8d4cb-152">Devuelve una lista ordenada de los identificadores de entrada de los contenedores que se deben incluir en el proceso de resolución de nombres iniciado por el método [ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="8d4cb-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="8d4cb-154">Establece una nueva ruta de acceso de búsqueda en el perfil que se usa para el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="8d4cb-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="8d4cb-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="8d4cb-156">Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d4cb-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d4cb-157">See also</span></span>



[<span data-ttu-id="8d4cb-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8d4cb-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

