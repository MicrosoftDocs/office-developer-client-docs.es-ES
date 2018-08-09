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
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817085"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="f2027-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f2027-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="f2027-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2027-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2027-105">Proporciona acceso a los contenedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f2027-105">Provides access to address book containers.</span></span> <span data-ttu-id="f2027-106">MAPI y las aplicaciones cliente llame a los métodos de **IABContainer** para realizar la resolución de nombres y para crear, copiar y eliminación a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f2027-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2027-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f2027-107">Header file:</span></span>  <br/> |<span data-ttu-id="f2027-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2027-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f2027-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="f2027-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="f2027-110">Objetos de contenedor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f2027-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="f2027-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f2027-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f2027-112">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f2027-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="f2027-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f2027-113">Called by:</span></span>  <br/> |<span data-ttu-id="f2027-114">MAPI y las aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="f2027-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="f2027-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="f2027-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f2027-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="f2027-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="f2027-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="f2027-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="f2027-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="f2027-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="f2027-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="f2027-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="f2027-120">Negocian</span><span class="sxs-lookup"><span data-stu-id="f2027-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f2027-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="f2027-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f2027-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f2027-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="f2027-123">Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="f2027-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="f2027-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="f2027-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="f2027-125">Copia las entradas de uno o más, los usuarios normalmente mensajería o listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="f2027-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="f2027-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="f2027-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="f2027-127">Quita una o más entradas, normalmente otros contenedores, listas de distribución o a los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="f2027-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="f2027-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="f2027-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="f2027-129">Realiza la resolución de nombres para una o más entradas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f2027-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="f2027-130">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="f2027-130">**Required properties**</span></span>|<span data-ttu-id="f2027-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="f2027-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2027-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-133">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f2027-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="f2027-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-135">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f2027-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="f2027-136">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="f2027-142">**Propiedades opcionales**</span><span class="sxs-lookup"><span data-stu-id="f2027-142">**Optional properties**</span></span>|<span data-ttu-id="f2027-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="f2027-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2027-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2027-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2027-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2027-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2027-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2027-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2027-154">Remarks</span></span>

<span data-ttu-id="f2027-155">La interfaz de **IABContainer** indirectamente hereda de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) a través de la [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) y [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="f2027-155">The **IABContainer** interface inherits indirectly from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="f2027-156">Los proveedores de la libreta de direcciones implementan la interfaz de **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="f2027-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="f2027-157">Puede existir cualquier número de objetos de mensajería de usuario, listas de distribución y otros contenedores de libretas de direcciones en un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f2027-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="f2027-158">Al igual que con cualquier contenedor, los clientes o proveedores de servicios pueden usar un contenedor de la libreta de direcciones para abrir una de sus entradas o para recuperar una tabla de jerarquías o una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="f2027-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="f2027-159">Contenedores de la libreta de direcciones también proporcionan resolución de nombres y, según el proveedor, la capacidad de agregar, quitar o modificar las entradas.</span><span class="sxs-lookup"><span data-stu-id="f2027-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="f2027-160">MAPI define un contenedor de libreta de direcciones especial denominado la libreta de direcciones personales (PAB) que contiene las entradas que se copió desde otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="f2027-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="f2027-161">Una PAB siempre es modificable.</span><span class="sxs-lookup"><span data-stu-id="f2027-161">A PAB is always modifiable.</span></span> <span data-ttu-id="f2027-162">Normalmente, los usuarios rellenan su PAB con las entradas de la designación de los destinatarios con el que se comunican con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="f2027-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="f2027-163">Una PAB también puede contener direcciones de uso único y nuevos destinatarios todavía no está una parte de cualquier contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f2027-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2027-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2027-164">See also</span></span>

- [<span data-ttu-id="f2027-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f2027-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

