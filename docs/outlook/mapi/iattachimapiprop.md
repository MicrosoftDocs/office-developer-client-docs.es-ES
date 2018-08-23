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
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570915"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="c39d3-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c39d3-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="c39d3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c39d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c39d3-105">Mantiene y proporciona acceso a las propiedades de los datos adjuntos en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c39d3-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="c39d3-106">La interfaz **IAttach** no tiene únicos métodos de su propio.</span><span class="sxs-lookup"><span data-stu-id="c39d3-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="c39d3-107">Para obtener más información acerca de cómo usar los datos adjuntos, vea [Los datos adjuntos de MAPI](mapi-attachments.md) y [Las tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c39d3-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c39d3-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c39d3-108">Header file:</span></span>  <br/> |<span data-ttu-id="c39d3-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c39d3-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c39d3-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="c39d3-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="c39d3-111">Objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="c39d3-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="c39d3-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c39d3-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c39d3-113">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c39d3-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="c39d3-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c39d3-114">Called by:</span></span>  <br/> |<span data-ttu-id="c39d3-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="c39d3-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="c39d3-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="c39d3-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c39d3-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="c39d3-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="c39d3-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="c39d3-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="c39d3-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="c39d3-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="c39d3-120">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="c39d3-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="c39d3-121">Negocian</span><span class="sxs-lookup"><span data-stu-id="c39d3-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c39d3-122">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="c39d3-122">Vtable order</span></span>

<span data-ttu-id="c39d3-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="c39d3-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="c39d3-124">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="c39d3-124">**Required properties**</span></span>|<span data-ttu-id="c39d3-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="c39d3-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c39d3-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c39d3-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c39d3-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c39d3-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="c39d3-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c39d3-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c39d3-129">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c39d3-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="c39d3-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c39d3-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c39d3-131">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c39d3-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c39d3-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c39d3-132">See also</span></span>



[<span data-ttu-id="c39d3-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c39d3-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

