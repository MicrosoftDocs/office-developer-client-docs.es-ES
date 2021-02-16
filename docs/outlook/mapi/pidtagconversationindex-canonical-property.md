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
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334723"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="cc94c-103">Propiedad canónica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="cc94c-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="cc94c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc94c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc94c-105">Contiene un valor binario que indica la posición relativa de este mensaje dentro de un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="cc94c-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc94c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc94c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc94c-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="cc94c-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="cc94c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc94c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc94c-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="cc94c-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="cc94c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cc94c-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc94c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc94c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc94c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc94c-112">Area:</span></span>  <br/> |<span data-ttu-id="cc94c-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="cc94c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc94c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc94c-114">Remarks</span></span>

<span data-ttu-id="cc94c-115">Un hilo de conversación representa una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="cc94c-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="cc94c-116">Esta propiedad normalmente se implementa mediante valores de marca de tiempo concatenados.</span><span class="sxs-lookup"><span data-stu-id="cc94c-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="cc94c-117">Su uso es opcional, incluso **si PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) está establecido.</span><span class="sxs-lookup"><span data-stu-id="cc94c-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="cc94c-118">MAPI proporciona la [función ScCreateConversationIndex](sccreateconversationindex.md) para crear o actualizar un índice de conversación.</span><span class="sxs-lookup"><span data-stu-id="cc94c-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="cc94c-119">La función toma el valor de índice actual como una matriz de bytes contada y devuelve el valor de índice con una marca de tiempo concatenada al final.</span><span class="sxs-lookup"><span data-stu-id="cc94c-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="cc94c-120">Un mensaje que representa una respuesta a otro mensaje debe usar **ScCreateConversationIndex** para actualizar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc94c-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="cc94c-121">Un proveedor de al almacenamiento de  mensajes tiene la opción de asegurar que PR_CONVERSATION_INDEX se establece siempre en los mensajes entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="cc94c-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="cc94c-122">Puede hacerlo llamando a **ScCreateConversationIndex**, ya sea con el valor existente si esta propiedad está establecida o con NULL si no lo está.</span><span class="sxs-lookup"><span data-stu-id="cc94c-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="cc94c-123">Esta acción debe realizarse antes [de llamar a IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="cc94c-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="cc94c-124">Todos los mensajes que tienen el mismo valor para **PR_CONVERSATION_TOPIC** pueden ordenarse en esta propiedad para revelar la relación jerárquica de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cc94c-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc94c-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc94c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc94c-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cc94c-126">Protocol specifications</span></span>

<span data-ttu-id="cc94c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc94c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc94c-128">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cc94c-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc94c-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc94c-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc94c-130">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cc94c-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc94c-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc94c-131">Header files</span></span>

<span data-ttu-id="cc94c-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc94c-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc94c-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc94c-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc94c-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc94c-134">Mapitags.h</span></span>
  
> <span data-ttu-id="cc94c-135">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc94c-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc94c-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc94c-136">See also</span></span>



[<span data-ttu-id="cc94c-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc94c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc94c-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cc94c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc94c-139">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc94c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc94c-140">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cc94c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

