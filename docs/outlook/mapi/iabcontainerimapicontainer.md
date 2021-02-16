---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348961"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="d3d8d-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d3d8d-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="d3d8d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3d8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3d8d-105">Proporciona acceso a contenedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-105">Provides access to address book containers.</span></span> <span data-ttu-id="d3d8d-106">MAPI y las aplicaciones cliente llaman a los métodos de **IABContainer** para realizar la resolución de nombres y para crear, copiar y eliminar destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3d8d-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-107">Header file:</span></span>  <br/> |<span data-ttu-id="d3d8d-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3d8d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d3d8d-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="d3d8d-110">Objetos contenedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d3d8d-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="d3d8d-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3d8d-112">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="d3d8d-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="d3d8d-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-113">Called by:</span></span>  <br/> |<span data-ttu-id="d3d8d-114">MAPI y aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="d3d8d-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="d3d8d-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d3d8d-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="d3d8d-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="d3d8d-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="d3d8d-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="d3d8d-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="d3d8d-119">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="d3d8d-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="d3d8d-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="d3d8d-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d3d8d-121">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="d3d8d-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d3d8d-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="d3d8d-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="d3d8d-123">Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="d3d8d-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="d3d8d-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="d3d8d-125">Copia una o más entradas, normalmente usuarios de mensajería o listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="d3d8d-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="d3d8d-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="d3d8d-127">Quita una o más entradas, normalmente usuarios de mensajería, listas de distribución u otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="d3d8d-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="d3d8d-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="d3d8d-129">Realiza la resolución de nombres para una o varias entradas de destinatario.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="d3d8d-130">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="d3d8d-130">**Required properties**</span></span>|<span data-ttu-id="d3d8d-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="d3d8d-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3d8d-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="d3d8d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="d3d8d-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="d3d8d-142">**Propiedades opcionales**</span><span class="sxs-lookup"><span data-stu-id="d3d8d-142">**Optional properties**</span></span>|<span data-ttu-id="d3d8d-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="d3d8d-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3d8d-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3d8d-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3d8d-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3d8d-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3d8d-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3d8d-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3d8d-154">Remarks</span></span>

<span data-ttu-id="d3d8d-155">La **interfaz IABContainer** hereda indirectamente de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) a través de [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp : interfaces IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="d3d8d-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="d3d8d-156">Los proveedores de libretas de direcciones implementan **la interfaz IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="d3d8d-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="d3d8d-157">Cualquier número de objetos de usuario de mensajería, listas de distribución y otros contenedores de libreta de direcciones puede existir en un contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="d3d8d-158">Al igual que con cualquier contenedor, los clientes o proveedores de servicios pueden usar un contenedor de libreta de direcciones para abrir una de sus entradas o para recuperar una tabla de jerarquía o una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="d3d8d-159">Los contenedores de libreta de direcciones también proporcionan resolución de nombres y, según el proveedor, la capacidad de agregar, quitar o modificar entradas.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="d3d8d-160">MAPI define un contenedor de libreta de direcciones especial denominado libreta de direcciones personal (PAB) que contiene las entradas copiadas de otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="d3d8d-161">Un PAB siempre se puede modifica.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-161">A PAB is always modifiable.</span></span> <span data-ttu-id="d3d8d-162">Normalmente, los usuarios rellenan su PAB con entradas que designan a los destinatarios con los que se comunican con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="d3d8d-163">Una PAB también puede contener direcciones de uso único y destinatarios nuevos que aún no forman parte de ningún contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d3d8d-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3d8d-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d3d8d-164">See also</span></span>

- [<span data-ttu-id="d3d8d-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d3d8d-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

