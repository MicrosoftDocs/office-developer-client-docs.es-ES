---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409093"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="5143d-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5143d-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="5143d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5143d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5143d-105">Mantiene y proporciona acceso a las propiedades de los datos adjuntos de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5143d-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="5143d-106">La interfaz **IAttach** no tiene métodos únicos propios.</span><span class="sxs-lookup"><span data-stu-id="5143d-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="5143d-107">Para obtener más información acerca de cómo usar los datos adjuntos, consulte datos adjuntos de [MAPI](mapi-attachments.md) y [tablas de datos](attachment-tables.md)adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5143d-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5143d-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5143d-108">Header file:</span></span>  <br/> |<span data-ttu-id="5143d-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5143d-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5143d-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="5143d-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="5143d-111">Objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="5143d-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="5143d-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5143d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="5143d-113">Proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="5143d-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="5143d-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5143d-114">Called by:</span></span>  <br/> |<span data-ttu-id="5143d-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="5143d-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="5143d-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5143d-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5143d-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="5143d-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="5143d-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="5143d-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="5143d-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="5143d-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="5143d-120">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="5143d-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="5143d-121">Negocian</span><span class="sxs-lookup"><span data-stu-id="5143d-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5143d-122">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5143d-122">Vtable order</span></span>

<span data-ttu-id="5143d-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="5143d-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="5143d-124">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="5143d-124">**Required properties**</span></span>|<span data-ttu-id="5143d-125">**Acceso**</span><span class="sxs-lookup"><span data-stu-id="5143d-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5143d-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5143d-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5143d-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5143d-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="5143d-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5143d-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5143d-129">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5143d-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="5143d-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5143d-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5143d-131">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="5143d-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5143d-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="5143d-132">See also</span></span>



[<span data-ttu-id="5143d-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5143d-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

