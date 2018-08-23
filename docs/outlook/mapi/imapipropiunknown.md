---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583732"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="45dd0-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45dd0-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="45dd0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45dd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45dd0-105">Permite a los clientes, proveedores de servicios y MAPI trabajar con propiedades.</span><span class="sxs-lookup"><span data-stu-id="45dd0-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="45dd0-106">Todos los objetos que admiten propiedades implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="45dd0-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45dd0-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="45dd0-107">Header file:</span></span>  <br/> |<span data-ttu-id="45dd0-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45dd0-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="45dd0-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="45dd0-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="45dd0-110">No hay ningún objeto expone esta interfaz directamente.</span><span class="sxs-lookup"><span data-stu-id="45dd0-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="45dd0-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="45dd0-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="45dd0-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="45dd0-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="45dd0-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="45dd0-113">Called by:</span></span>  <br/> |<span data-ttu-id="45dd0-114">Las aplicaciones cliente, los proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="45dd0-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="45dd0-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="45dd0-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="45dd0-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="45dd0-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="45dd0-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="45dd0-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="45dd0-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="45dd0-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="45dd0-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="45dd0-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="45dd0-120">Clase abstracta, que nunca se ha implementado</span><span class="sxs-lookup"><span data-stu-id="45dd0-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="45dd0-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="45dd0-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="45dd0-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="45dd0-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="45dd0-123">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior.</span><span class="sxs-lookup"><span data-stu-id="45dd0-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="45dd0-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="45dd0-125">Hace permanentes los cambios realizados a un objeto desde la última operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="45dd0-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="45dd0-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="45dd0-127">Recupera el valor de la propiedad de una o varias propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="45dd0-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="45dd0-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="45dd0-129">Devuelve las etiquetas de propiedad para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="45dd0-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="45dd0-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="45dd0-131">Devuelve un puntero a una interfaz que se puede usar para obtener acceso a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="45dd0-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="45dd0-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="45dd0-133">Actualiza las propiedades de uno o más.</span><span class="sxs-lookup"><span data-stu-id="45dd0-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="45dd0-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="45dd0-135">Elimina una o más propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="45dd0-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="45dd0-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="45dd0-137">Copia o mueve todas las propiedades, excepto propiedades excluidas específicamente.</span><span class="sxs-lookup"><span data-stu-id="45dd0-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="45dd0-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="45dd0-139">Copia o mueve las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="45dd0-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="45dd0-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="45dd0-141">Proporciona los nombres de propiedad que se corresponden con uno o varios identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="45dd0-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="45dd0-142">A GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="45dd0-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="45dd0-143">Proporciona los identificadores de propiedad que se corresponden con uno o varios nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="45dd0-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45dd0-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45dd0-144">Remarks</span></span>

 <span data-ttu-id="45dd0-145">**IMAPIProp** es la interfaz base para las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="45dd0-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="45dd0-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="45dd0-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="45dd0-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="45dd0-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="45dd0-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="45dd0-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="45dd0-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="45dd0-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="45dd0-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="45dd0-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="45dd0-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="45dd0-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="45dd0-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="45dd0-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="45dd0-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="45dd0-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="45dd0-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="45dd0-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="45dd0-155">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="45dd0-155">See also</span></span>



[<span data-ttu-id="45dd0-156">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="45dd0-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

