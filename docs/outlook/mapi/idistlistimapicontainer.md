---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431550"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="e5e3f-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e5e3f-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="e5e3f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5e3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5e3f-105">Proporciona acceso a listas de distribución en contenedores modificables de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="e5e3f-106">**IDistList puede** crear, copiar y eliminar listas de distribución, además de realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5e3f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-107">Header file:</span></span>  <br/> |<span data-ttu-id="e5e3f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5e3f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e5e3f-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e5e3f-110">Objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="e5e3f-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="e5e3f-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5e3f-112">Proveedores de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e5e3f-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="e5e3f-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-113">Called by:</span></span>  <br/> |<span data-ttu-id="e5e3f-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="e5e3f-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="e5e3f-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e5e3f-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="e5e3f-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="e5e3f-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e5e3f-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="e5e3f-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="e5e3f-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="e5e3f-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="e5e3f-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e5e3f-121">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="e5e3f-121">Vtable order</span></span>

<span data-ttu-id="e5e3f-122">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="e5e3f-123">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="e5e3f-123">**Required properties**</span></span>|<span data-ttu-id="e5e3f-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="e5e3f-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5e3f-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5e3f-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e5e3f-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="e5e3f-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5e3f-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e5e3f-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="e5e3f-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5e3f-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5e3f-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="e5e3f-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5e3f-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5e3f-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="e5e3f-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5e3f-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5e3f-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5e3f-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5e3f-135">Remarks</span></span>

<span data-ttu-id="e5e3f-136">La **interfaz IDistList** hereda de [IMAPIContainer](imapicontainerimapiprop.md) e incluye los mismos métodos que los contenedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="e5e3f-137">Por lo tanto, dado que los métodos de la **interfaz IDistList** son idénticos a los de la [interfaz IABContainer,](iabcontainerimapicontainer.md) no se duplican aquí.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="e5e3f-138">Una lista de distribución u objeto que implementa **IDistList** es una colección de objetos de usuario de mensajería o destinatarios individuales.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="e5e3f-139">Una lista de distribución puede estar formada por todos los objetos de usuario de mensajería, o algunos usuarios de mensajería y algunas listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="e5e3f-140">Normalmente hay dos tipos de listas de distribución:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="e5e3f-141">Listas de distribución expandida por el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="e5e3f-142">Este tipo de lista tiene una dirección, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), y se trata igual que si fuera un destinatario individual.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="e5e3f-143">Listas de distribución que existen en un contenedor local y que la aplicación cliente expande.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="e5e3f-144">Entre las propiedades de lista de distribución opcionales se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5e3f-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="e5e3f-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="e5e3f-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="e5e3f-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5e3f-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="e5e3f-148">Observe que **PR_ADDRTYPE** es necesario, pero **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) no lo es.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="e5e3f-149">Esto se debe a que una lista de distribución sin una dirección de correo electrónico todavía puede recibir mensajes, pero su lista de miembros debe expandirse.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="e5e3f-150">Si la **PR_ADDRTYPE** está establecida en MAPIPDL, MAPI realiza la expansión.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="e5e3f-151">Si **PR_ADDRTYPE** es un valor distinto de MAPIPDL, el proveedor de transporte realiza la expansión.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="e5e3f-152">Para obtener información adicional acerca de cómo usar los **métodos IDistList,** vea las entradas de referencia para los métodos paralelos de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="e5e3f-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5e3f-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5e3f-153">See also</span></span>



[<span data-ttu-id="e5e3f-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e5e3f-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

