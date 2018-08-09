---
title: Propiedad canónica PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819750"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="26593-103">Propiedad canónica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="26593-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="26593-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26593-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26593-105">Contiene la suma, en bytes, de los tamaños de todas las propiedades en un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="26593-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26593-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="26593-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26593-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="26593-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="26593-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="26593-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26593-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="26593-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="26593-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="26593-110">Data type:</span></span>  <br/> |<span data-ttu-id="26593-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="26593-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="26593-112">Área:</span><span class="sxs-lookup"><span data-stu-id="26593-112">Area:</span></span>  <br/> |<span data-ttu-id="26593-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="26593-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26593-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26593-114">Remarks</span></span>

<span data-ttu-id="26593-115">Se recomienda que los objetos de mensaje exponen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="26593-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="26593-116">El tamaño de mensaje indica el número aproximado de bytes que se transfieren cuando el mensaje se mueve de almacén de mensajes de uno a otro.</span><span class="sxs-lookup"><span data-stu-id="26593-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="26593-117">Que se va a la suma de los tamaños de todas las propiedades en el objeto de mensaje, normalmente es considerablemente mayor que el texto del mensaje por sí solo.</span><span class="sxs-lookup"><span data-stu-id="26593-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="26593-118">Del almacén de mensajes mayoría proveedores compute esta propiedad para mensajes que controlan.</span><span class="sxs-lookup"><span data-stu-id="26593-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="26593-119">Sin embargo, algunos proveedores de almacén de mensajes no admiten esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="26593-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="26593-120">En cualquier caso, esta propiedad no está disponible hasta que se ha llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="26593-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="26593-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="26593-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26593-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="26593-122">Protocol specifications</span></span>

<span data-ttu-id="26593-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26593-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26593-124">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="26593-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26593-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26593-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26593-126">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="26593-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="26593-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26593-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26593-128">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="26593-128">Handles folder operations.</span></span>
    
<span data-ttu-id="26593-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26593-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26593-130">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="26593-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26593-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="26593-131">Header files</span></span>

<span data-ttu-id="26593-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26593-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="26593-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="26593-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="26593-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26593-134">Mapitags.h</span></span>
  
> <span data-ttu-id="26593-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="26593-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26593-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="26593-136">See also</span></span>



[<span data-ttu-id="26593-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="26593-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26593-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="26593-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26593-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="26593-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26593-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="26593-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

