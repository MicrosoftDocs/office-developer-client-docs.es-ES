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
ms.openlocfilehash: ce9d13b6ecd560798cee4f79d8d62b966dc427f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586476"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="f4548-103">Propiedad canónica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f4548-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="f4548-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4548-105">Contiene el tema del primer mensaje en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="f4548-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4548-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f4548-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4548-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="f4548-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="f4548-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f4548-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4548-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="f4548-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="f4548-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f4548-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4548-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4548-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4548-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f4548-112">Area:</span></span>  <br/> |<span data-ttu-id="f4548-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="f4548-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4548-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4548-114">Remarks</span></span>

<span data-ttu-id="f4548-115">Un subproceso de conversación representa una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="f4548-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="f4548-116">Estas propiedades se establecen para el primer mensaje de un subproceso, por lo general a la propiedad **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4548-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="f4548-117">Los mensajes subsiguientes en el subproceso deben usar el mismo tema sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="f4548-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="f4548-118">La propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica la relación de orden entre los mensajes subsiguientes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="f4548-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="f4548-119">Su uso es opcional, incluso si se establecen estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f4548-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="f4548-120">Un proveedor de almacén de mensajes tiene la opción de garantizar que siempre se establecen estas propiedades en los mensajes entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="f4548-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="f4548-121">Si ya se establecen estas propiedades no se debe modificar.</span><span class="sxs-lookup"><span data-stu-id="f4548-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="f4548-122">Si no es así, se puede establecer en **PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="f4548-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="f4548-123">Antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , se debe realizar cualquier acción.</span><span class="sxs-lookup"><span data-stu-id="f4548-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4548-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4548-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4548-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f4548-125">Protocol specifications</span></span>

<span data-ttu-id="f4548-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4548-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4548-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f4548-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4548-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4548-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4548-129">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f4548-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4548-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f4548-130">Header files</span></span>

<span data-ttu-id="f4548-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4548-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4548-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f4548-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4548-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4548-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f4548-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f4548-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4548-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f4548-135">See also</span></span>



[<span data-ttu-id="f4548-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4548-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4548-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f4548-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4548-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f4548-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4548-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f4548-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

