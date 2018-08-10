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
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817187"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="25ff0-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="25ff0-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="25ff0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25ff0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25ff0-105">Proporciona acceso a listas de distribución en dirección modificable contenedores de libretas.</span><span class="sxs-lookup"><span data-stu-id="25ff0-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="25ff0-106">**IDistList** puede crear, copiar y eliminar listas de distribución, además de realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="25ff0-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25ff0-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="25ff0-107">Header file:</span></span>  <br/> |<span data-ttu-id="25ff0-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25ff0-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25ff0-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="25ff0-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="25ff0-110">Objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="25ff0-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="25ff0-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="25ff0-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="25ff0-112">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="25ff0-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="25ff0-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="25ff0-113">Called by:</span></span>  <br/> |<span data-ttu-id="25ff0-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="25ff0-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="25ff0-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="25ff0-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="25ff0-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="25ff0-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="25ff0-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="25ff0-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="25ff0-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="25ff0-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="25ff0-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="25ff0-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="25ff0-120">Negocian</span><span class="sxs-lookup"><span data-stu-id="25ff0-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="25ff0-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="25ff0-121">Vtable order</span></span>

<span data-ttu-id="25ff0-122">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="25ff0-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="25ff0-123">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="25ff0-123">**Required properties**</span></span>|<span data-ttu-id="25ff0-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="25ff0-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25ff0-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25ff0-126">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="25ff0-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="25ff0-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25ff0-128">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="25ff0-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="25ff0-129">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25ff0-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="25ff0-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="25ff0-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25ff0-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="25ff0-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="25ff0-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="25ff0-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="25ff0-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25ff0-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25ff0-135">Remarks</span></span>

<span data-ttu-id="25ff0-136">La interfaz de **IDistList** hereda de [IMAPIContainer](imapicontainerimapiprop.md) e incluye los mismos métodos que los contenedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="25ff0-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="25ff0-137">Por lo tanto, debido a que los métodos de la interfaz de **IDistList** son idénticos a las de la interfaz [IABContainer](iabcontainerimapicontainer.md) , no se duplican aquí.</span><span class="sxs-lookup"><span data-stu-id="25ff0-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="25ff0-138">Una lista de distribución o un objeto que implementa **IDistList** es una colección de objetos de usuario de mensajería o destinatarios individuales.</span><span class="sxs-lookup"><span data-stu-id="25ff0-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="25ff0-139">Una lista de distribución puede constar de todos los objetos de usuario mensajería, o algún usuario de mensajería y algunas listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="25ff0-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="25ff0-140">Normalmente, existen dos tipos de listas de distribución:</span><span class="sxs-lookup"><span data-stu-id="25ff0-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="25ff0-141">En las listas de distribución se expanden por el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="25ff0-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="25ff0-142">Este tipo de lista tiene una dirección, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y es el mismo se trata como si fuese un destinatario individual.</span><span class="sxs-lookup"><span data-stu-id="25ff0-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="25ff0-143">Listas de distribución que existen en un contenedor local y se expanden por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="25ff0-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="25ff0-144">Propiedades de la lista de distribución opcional incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="25ff0-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="25ff0-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="25ff0-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25ff0-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25ff0-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="25ff0-148">Observe que **PR_ADDRTYPE** es necesario, pero no es de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25ff0-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="25ff0-149">Eso es porque una lista de distribución sin una dirección de correo electrónico puede seguir recibiendo mensajes, pero se debe expandir la lista de miembros.</span><span class="sxs-lookup"><span data-stu-id="25ff0-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="25ff0-150">Si se establece la propiedad **PR_ADDRTYPE** en MAPIPDL, MAPI realiza la expansión.</span><span class="sxs-lookup"><span data-stu-id="25ff0-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="25ff0-151">Si **PR_ADDRTYPE** es un valor distinto de MAPIPDL, el proveedor de transporte lleva a cabo la expansión.</span><span class="sxs-lookup"><span data-stu-id="25ff0-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="25ff0-152">Para obtener información adicional acerca de cómo usar los métodos **IDistList** , vea las entradas de referencia para los métodos paralelos de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="25ff0-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25ff0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="25ff0-153">See also</span></span>



[<span data-ttu-id="25ff0-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="25ff0-154">MAPI Interfaces</span></span>](mapi-interfaces.md)
