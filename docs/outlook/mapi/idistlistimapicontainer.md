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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350893"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="1f163-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1f163-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="1f163-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f163-105">Proporciona acceso a las listas de distribución en contenedores de libretas de direcciones modificables.</span><span class="sxs-lookup"><span data-stu-id="1f163-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="1f163-106">**IDistList** puede crear, copiar y eliminar listas de distribución, además de realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="1f163-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f163-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1f163-107">Header file:</span></span>  <br/> |<span data-ttu-id="1f163-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1f163-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1f163-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="1f163-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="1f163-110">Objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="1f163-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="1f163-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1f163-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1f163-112">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="1f163-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="1f163-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1f163-113">Called by:</span></span>  <br/> |<span data-ttu-id="1f163-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="1f163-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="1f163-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1f163-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1f163-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="1f163-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="1f163-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="1f163-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="1f163-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="1f163-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="1f163-119">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="1f163-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="1f163-120">Negocian</span><span class="sxs-lookup"><span data-stu-id="1f163-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1f163-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="1f163-121">Vtable order</span></span>

<span data-ttu-id="1f163-122">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="1f163-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="1f163-123">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="1f163-123">**Required properties**</span></span>|<span data-ttu-id="1f163-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="1f163-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f163-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f163-126">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="1f163-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="1f163-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f163-128">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="1f163-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="1f163-129">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f163-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f163-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="1f163-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f163-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f163-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="1f163-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f163-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f163-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f163-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f163-135">Remarks</span></span>

<span data-ttu-id="1f163-136">La interfaz **IDistList** hereda de [IMAPIContainer](imapicontainerimapiprop.md) e incluye los mismos métodos que los contenedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1f163-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="1f163-137">Por lo tanto, dado que los métodos de la interfaz **IDistList** son idénticos a los de la interfaz [IABContainer](iabcontainerimapicontainer.md) , no se duplican aquí.</span><span class="sxs-lookup"><span data-stu-id="1f163-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="1f163-138">Una lista de distribución o un objeto que implementa **IDistList** es una colección de objetos de usuario de mensajería o destinatarios individuales.</span><span class="sxs-lookup"><span data-stu-id="1f163-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="1f163-139">Una lista de distribución puede constar de todos los objetos de usuario de mensajería o algún usuario de mensajería y algunas listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="1f163-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="1f163-140">Normalmente, hay dos tipos de listas de distribución:</span><span class="sxs-lookup"><span data-stu-id="1f163-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="1f163-141">Listas de distribución expandidas por el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="1f163-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="1f163-142">Este tipo de lista tiene una dirección, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y se trata del mismo modo que si fuera un destinatario individual.</span><span class="sxs-lookup"><span data-stu-id="1f163-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="1f163-143">Listas de distribución que existen en un contenedor local y que se expanden mediante la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="1f163-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="1f163-144">Las propiedades de la lista de distribución opcional son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="1f163-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="1f163-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="1f163-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="1f163-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f163-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="1f163-148">Observe que **PR_ADDRTYPE** es necesario, pero **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) no lo es.</span><span class="sxs-lookup"><span data-stu-id="1f163-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="1f163-149">Esto se debe a que una lista de distribución sin una dirección de correo electrónico todavía puede recibir mensajes, pero su lista de miembros debe estar expandida.</span><span class="sxs-lookup"><span data-stu-id="1f163-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="1f163-150">Si la propiedad **PR_ADDRTYPE** se establece en MAPIPDL, MAPI realiza la expansión.</span><span class="sxs-lookup"><span data-stu-id="1f163-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="1f163-151">Si **PR_ADDRTYPE** es un valor distinto de MAPIPDL, el proveedor de transporte realiza la expansión.</span><span class="sxs-lookup"><span data-stu-id="1f163-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="1f163-152">Para obtener más información acerca de cómo usar los métodos **IDistList** , vea las entradas de referencia para los métodos paralelos de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="1f163-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f163-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f163-153">See also</span></span>



[<span data-ttu-id="1f163-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1f163-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

