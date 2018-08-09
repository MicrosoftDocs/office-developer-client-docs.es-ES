---
title: Propiedad canónica PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bddb667cba99e240a6ce182c9c1c8ed47f467e15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819384"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="6a3f3-103">Propiedad canónica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="6a3f3-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="6a3f3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a3f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a3f3-105">Contiene un valor binario que indica la posición relativa de este mensaje dentro de una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a3f3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6a3f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a3f3-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="6a3f3-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="6a3f3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6a3f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a3f3-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="6a3f3-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="6a3f3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6a3f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a3f3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a3f3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6a3f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6a3f3-112">Area:</span></span>  <br/> |<span data-ttu-id="6a3f3-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="6a3f3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a3f3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a3f3-114">Remarks</span></span>

<span data-ttu-id="6a3f3-115">Un subproceso de conversación representa una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="6a3f3-116">Esta propiedad normalmente se implementa mediante los valores de marca de tiempo concatenado.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="6a3f3-117">Su uso es opcional, incluso si se establece **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6a3f3-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="6a3f3-118">MAPI proporciona la función [ScCreateConversationIndex](sccreateconversationindex.md) para crear o actualizar un índice de conversación.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="6a3f3-119">La función toma el valor de índice actual como una matriz de bytes contada y devuelve el valor de índice con una marca de tiempo concatenada al final.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="6a3f3-120">Un mensaje que representa una respuesta a otro mensaje debe usar **ScCreateConversationIndex** para actualizar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="6a3f3-121">Un proveedor de almacén de mensajes tiene la opción de garantizar que **PR_CONVERSATION_INDEX** siempre se establece en los mensajes entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="6a3f3-122">Puede hacerlo mediante una llamada a **ScCreateConversationIndex**, con el valor existente si se establece esta propiedad o con el valor NULL si no lo está.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="6a3f3-123">Antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , se debe realizar esta acción.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="6a3f3-124">Todos los mensajes que tienen el mismo valor para **PR_CONVERSATION_TOPIC** se pueden ordenar en esta propiedad para mostrar la relación jerárquica de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6a3f3-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a3f3-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a3f3-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6a3f3-126">Protocol specifications</span></span>

<span data-ttu-id="6a3f3-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a3f3-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a3f3-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a3f3-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a3f3-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a3f3-130">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a3f3-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6a3f3-131">Header files</span></span>

<span data-ttu-id="6a3f3-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a3f3-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a3f3-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a3f3-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a3f3-134">Mapitags.h</span></span>
  
> <span data-ttu-id="6a3f3-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a3f3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a3f3-136">See also</span></span>



[<span data-ttu-id="6a3f3-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6a3f3-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a3f3-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6a3f3-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a3f3-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6a3f3-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a3f3-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6a3f3-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

