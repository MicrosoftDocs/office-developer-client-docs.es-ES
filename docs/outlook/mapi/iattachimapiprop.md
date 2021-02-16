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
# <a name="iattach--imapiprop"></a><span data-ttu-id="1de02-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1de02-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="1de02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1de02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1de02-105">Mantiene y proporciona acceso a las propiedades de los datos adjuntos de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1de02-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="1de02-106">La **interfaz IAttach** no tiene métodos únicos propios.</span><span class="sxs-lookup"><span data-stu-id="1de02-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="1de02-107">Para obtener más información acerca de cómo usar datos adjuntos, vea Datos adjuntos [mapi](mapi-attachments.md) y [tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1de02-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1de02-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1de02-108">Header file:</span></span>  <br/> |<span data-ttu-id="1de02-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1de02-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1de02-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="1de02-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1de02-111">Objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="1de02-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="1de02-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1de02-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1de02-113">Proveedores de al almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="1de02-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1de02-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1de02-114">Called by:</span></span>  <br/> |<span data-ttu-id="1de02-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="1de02-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="1de02-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1de02-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1de02-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="1de02-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="1de02-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="1de02-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="1de02-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="1de02-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="1de02-120">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="1de02-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="1de02-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="1de02-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1de02-122">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="1de02-122">Vtable order</span></span>

<span data-ttu-id="1de02-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="1de02-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="1de02-124">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="1de02-124">**Required properties**</span></span>|<span data-ttu-id="1de02-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="1de02-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1de02-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1de02-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1de02-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="1de02-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1de02-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1de02-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="1de02-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1de02-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1de02-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1de02-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1de02-132">See also</span></span>



[<span data-ttu-id="1de02-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1de02-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

