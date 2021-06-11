---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406125"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="34089-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="34089-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="34089-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34089-105">Administra operaciones de alto nivel en objetos contenedor, como libretas de direcciones, listas de distribución y carpetas.</span><span class="sxs-lookup"><span data-stu-id="34089-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="34089-106">Las [interfaces IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)y [IDistList : IMAPIContainer](idistlistimapicontainer.md) se derivan de **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="34089-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34089-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="34089-107">Header file:</span></span>  <br/> |<span data-ttu-id="34089-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34089-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="34089-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="34089-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="34089-110">Carpeta, contenedor de libreta de direcciones y objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="34089-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="34089-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="34089-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="34089-112">Proveedores de almacenamiento de mensajes, libreta de direcciones y transporte remoto</span><span class="sxs-lookup"><span data-stu-id="34089-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="34089-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="34089-113">Called by:</span></span>  <br/> |<span data-ttu-id="34089-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="34089-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="34089-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="34089-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="34089-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="34089-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="34089-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="34089-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="34089-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="34089-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="34089-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="34089-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="34089-120">Clase abstracta, nunca implementada</span><span class="sxs-lookup"><span data-stu-id="34089-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="34089-121">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="34089-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="34089-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="34089-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="34089-123">Devuelve un puntero a la tabla de contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="34089-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="34089-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="34089-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="34089-125">Devuelve un puntero a la tabla de jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="34089-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="34089-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="34089-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="34089-127">Abre un objeto en el contenedor y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="34089-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="34089-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="34089-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="34089-129">Establece criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="34089-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="34089-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="34089-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="34089-131">Obtiene los criterios de búsqueda del contenedor.</span><span class="sxs-lookup"><span data-stu-id="34089-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="34089-132">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="34089-132">**Required properties**</span></span>|<span data-ttu-id="34089-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="34089-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34089-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34089-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34089-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34089-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="34089-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34089-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34089-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34089-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="34089-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34089-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34089-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="34089-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34089-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="34089-140">See also</span></span>



[<span data-ttu-id="34089-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="34089-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

