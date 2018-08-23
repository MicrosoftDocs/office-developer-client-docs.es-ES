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
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575703"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="011cb-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="011cb-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="011cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="011cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="011cb-105">Administra las operaciones de alto nivel en objetos de contenedor como libretas de direcciones, listas de distribución y las carpetas.</span><span class="sxs-lookup"><span data-stu-id="011cb-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="011cb-106">El [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), y [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces se derivan de **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="011cb-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="011cb-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="011cb-107">Header file:</span></span>  <br/> |<span data-ttu-id="011cb-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="011cb-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="011cb-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="011cb-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="011cb-110">Carpeta, el contenedor de la libreta de direcciones y objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="011cb-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="011cb-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="011cb-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="011cb-112">Almacén de mensajes, la libreta de direcciones y los proveedores de transporte remoto</span><span class="sxs-lookup"><span data-stu-id="011cb-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="011cb-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="011cb-113">Called by:</span></span>  <br/> |<span data-ttu-id="011cb-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="011cb-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="011cb-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="011cb-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="011cb-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="011cb-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="011cb-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="011cb-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="011cb-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="011cb-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="011cb-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="011cb-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="011cb-120">Clase abstracta, que nunca se ha implementado</span><span class="sxs-lookup"><span data-stu-id="011cb-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="011cb-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="011cb-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="011cb-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="011cb-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="011cb-123">Devuelve un puntero a la tabla de contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="011cb-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="011cb-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="011cb-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="011cb-125">Devuelve un puntero a la tabla de jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="011cb-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="011cb-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="011cb-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="011cb-127">Abre un objeto en el contenedor, la devolución de un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="011cb-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="011cb-128">Es posible SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="011cb-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="011cb-129">Establece los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="011cb-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="011cb-130">Es posible GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="011cb-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="011cb-131">Obtiene los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="011cb-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="011cb-132">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="011cb-132">**Required properties**</span></span>|<span data-ttu-id="011cb-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="011cb-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="011cb-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="011cb-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="011cb-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="011cb-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="011cb-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="011cb-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="011cb-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="011cb-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="011cb-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="011cb-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="011cb-139">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="011cb-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="011cb-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="011cb-140">See also</span></span>



[<span data-ttu-id="011cb-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="011cb-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

