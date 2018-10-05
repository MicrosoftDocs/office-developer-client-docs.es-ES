---
title: Propiedad canónica PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400393"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="0edff-103">Propiedad canónica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="0edff-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="0edff-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0edff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0edff-105">Contiene el tema del primer mensaje en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="0edff-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0edff-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0edff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0edff-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="0edff-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="0edff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0edff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0edff-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="0edff-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="0edff-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0edff-110">Data type:</span></span>  <br/> |<span data-ttu-id="0edff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0edff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0edff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0edff-112">Area:</span></span>  <br/> |<span data-ttu-id="0edff-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="0edff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0edff-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0edff-114">Remarks</span></span>

<span data-ttu-id="0edff-115">Un subproceso de conversación representa una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="0edff-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="0edff-116">Estas propiedades se establecen para el primer mensaje de un subproceso, por lo general a la propiedad **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0edff-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="0edff-117">Los mensajes subsiguientes en el subproceso deben usar el mismo tema sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="0edff-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="0edff-118">La propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica la relación de orden entre los mensajes subsiguientes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="0edff-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="0edff-119">Su uso es opcional, incluso si se establecen estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0edff-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="0edff-120">Un proveedor de almacén de mensajes tiene la opción de garantizar que siempre se establecen estas propiedades en los mensajes entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="0edff-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="0edff-121">Si ya se establecen estas propiedades no se debe modificar.</span><span class="sxs-lookup"><span data-stu-id="0edff-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="0edff-122">Si no es así, se puede establecer en **PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="0edff-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="0edff-123">Antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , se debe realizar cualquier acción.</span><span class="sxs-lookup"><span data-stu-id="0edff-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0edff-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0edff-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0edff-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0edff-125">Protocol specifications</span></span>

<span data-ttu-id="0edff-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edff-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edff-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0edff-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0edff-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edff-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edff-129">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0edff-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0edff-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0edff-130">Header files</span></span>

<span data-ttu-id="0edff-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0edff-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0edff-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0edff-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0edff-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0edff-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0edff-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0edff-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0edff-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0edff-135">See also</span></span>



[<span data-ttu-id="0edff-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0edff-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0edff-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0edff-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0edff-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0edff-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0edff-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0edff-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

