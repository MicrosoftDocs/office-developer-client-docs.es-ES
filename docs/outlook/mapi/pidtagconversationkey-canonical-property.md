---
title: Propiedad canónica PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334702"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="8dd2f-103">Propiedad canónica PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="8dd2f-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="8dd2f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dd2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dd2f-105">Contiene la clave de conversación usada en Microsoft Outlook sólo cuando se busca **IPM. Mensajes MessageManager** , como el mensaje que contiene el historial de descargas de una cuenta de protocolo de oficina de correos (POP3).</span><span class="sxs-lookup"><span data-stu-id="8dd2f-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="8dd2f-106">Esta propiedad está en desuso en Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8dd2f-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8dd2f-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8dd2f-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="8dd2f-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="8dd2f-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8dd2f-109">Identifier:</span></span>  <br/> |<span data-ttu-id="8dd2f-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="8dd2f-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="8dd2f-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8dd2f-111">Data type:</span></span>  <br/> |<span data-ttu-id="8dd2f-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8dd2f-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8dd2f-113">Área:</span><span class="sxs-lookup"><span data-stu-id="8dd2f-113">Area:</span></span>  <br/> |<span data-ttu-id="8dd2f-114">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="8dd2f-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dd2f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8dd2f-115">Remarks</span></span>

<span data-ttu-id="8dd2f-116">Cuando se obtiene acceso a los mensajes de correo electrónico como conversaciones y se convierten las propiedades del mensaje al [formato de encapsulaCión neutro para el transporte (TNEF)](transport-neutral-encapsulation-format-tnef.md), no se debe usar esta propiedad; en su lugar, use las propiedades canónicas [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd2f-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8dd2f-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dd2f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8dd2f-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8dd2f-118">Protocol specifications</span></span>

<span data-ttu-id="8dd2f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dd2f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dd2f-120">Proporciona referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8dd2f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dd2f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dd2f-122">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="8dd2f-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dd2f-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dd2f-124">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8dd2f-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8dd2f-125">Header files</span></span>

<span data-ttu-id="8dd2f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8dd2f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8dd2f-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="8dd2f-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8dd2f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="8dd2f-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8dd2f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dd2f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dd2f-130">See also</span></span>



[<span data-ttu-id="8dd2f-131">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="8dd2f-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="8dd2f-132">Carpetas especiales de MAPI</span><span class="sxs-lookup"><span data-stu-id="8dd2f-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="8dd2f-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8dd2f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8dd2f-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8dd2f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8dd2f-135">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8dd2f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8dd2f-136">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8dd2f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

