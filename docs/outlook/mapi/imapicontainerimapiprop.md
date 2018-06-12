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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817209"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="a999c-103">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a999c-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="a999c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a999c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a999c-105">Administra las operaciones de alto nivel en objetos de contenedor como libretas de direcciones, listas de distribución y las carpetas.</span><span class="sxs-lookup"><span data-stu-id="a999c-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="a999c-106">El [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), y [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces se derivan de **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="a999c-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a999c-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a999c-107">Header file:</span></span>  <br/> |<span data-ttu-id="a999c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a999c-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a999c-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="a999c-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a999c-110">Carpeta, el contenedor de la libreta de direcciones y objetos de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="a999c-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="a999c-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a999c-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a999c-112">Almacén de mensajes, la libreta de direcciones y los proveedores de transporte remoto</span><span class="sxs-lookup"><span data-stu-id="a999c-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="a999c-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a999c-113">Called by:</span></span>  <br/> |<span data-ttu-id="a999c-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="a999c-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a999c-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a999c-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a999c-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a999c-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="a999c-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a999c-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a999c-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="a999c-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="a999c-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="a999c-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a999c-120">Clase abstracta, que nunca se ha implementado</span><span class="sxs-lookup"><span data-stu-id="a999c-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a999c-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="a999c-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a999c-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="a999c-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="a999c-123">Devuelve un puntero a la tabla de contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="a999c-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="a999c-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="a999c-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="a999c-125">Devuelve un puntero a la tabla de jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="a999c-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="a999c-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a999c-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="a999c-127">Abre un objeto en el contenedor, la devolución de un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="a999c-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="a999c-128">Es posible SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a999c-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="a999c-129">Establece los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a999c-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="a999c-130">Es posible GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a999c-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="a999c-131">Obtiene los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a999c-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="a999c-132">**Propiedades necesarias**</span><span class="sxs-lookup"><span data-stu-id="a999c-132">**Required properties**</span></span>|<span data-ttu-id="a999c-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="a999c-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a999c-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a999c-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a999c-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a999c-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="a999c-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a999c-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a999c-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a999c-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a999c-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a999c-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a999c-139">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a999c-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a999c-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="a999c-140">See also</span></span>



[<span data-ttu-id="a999c-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a999c-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

