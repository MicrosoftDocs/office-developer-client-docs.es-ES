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
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817141"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="d919b-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d919b-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="d919b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d919b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d919b-105">Mantiene y proporciona acceso a las propiedades de los datos adjuntos en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="d919b-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="d919b-106">La interfaz **IAttach** no tiene únicos métodos de su propio.</span><span class="sxs-lookup"><span data-stu-id="d919b-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="d919b-107">Para obtener más información acerca de cómo usar los datos adjuntos, vea [Los datos adjuntos de MAPI](mapi-attachments.md) y [Las tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d919b-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d919b-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d919b-108">Header file:</span></span>  <br/> |<span data-ttu-id="d919b-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d919b-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d919b-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="d919b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="d919b-111">Objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d919b-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="d919b-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d919b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="d919b-113">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="d919b-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="d919b-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d919b-114">Called by:</span></span>  <br/> |<span data-ttu-id="d919b-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="d919b-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="d919b-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d919b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d919b-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="d919b-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="d919b-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="d919b-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="d919b-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="d919b-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="d919b-120">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="d919b-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="d919b-121">Negocian</span><span class="sxs-lookup"><span data-stu-id="d919b-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d919b-122">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="d919b-122">Vtable order</span></span>

<span data-ttu-id="d919b-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="d919b-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="d919b-124">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="d919b-124">**Required properties**</span></span>|<span data-ttu-id="d919b-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="d919b-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d919b-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d919b-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d919b-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d919b-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="d919b-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d919b-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d919b-129">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d919b-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="d919b-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d919b-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d919b-131">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d919b-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d919b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d919b-132">See also</span></span>



[<span data-ttu-id="d919b-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d919b-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

