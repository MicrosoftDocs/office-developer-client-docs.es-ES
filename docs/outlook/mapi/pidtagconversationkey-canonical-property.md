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
ms.openlocfilehash: b4c8c6cf3bee0575a42bc42a1ebf5e185ef78ab4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591635"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="39fc1-103">Propiedad canónica PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="39fc1-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="39fc1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39fc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39fc1-105">Contiene la clave de conversación que se usa en Microsoft Outlook sólo al localizar **IPM. Objeto** mensajes, como el mensaje que contiene el historial de descarga para una cuenta de protocolo de oficina de correos (POP3).</span><span class="sxs-lookup"><span data-stu-id="39fc1-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="39fc1-106">Esta propiedad ha quedado obsoleto en Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="39fc1-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39fc1-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="39fc1-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="39fc1-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="39fc1-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="39fc1-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="39fc1-109">Identifier:</span></span>  <br/> |<span data-ttu-id="39fc1-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="39fc1-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="39fc1-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="39fc1-111">Data type:</span></span>  <br/> |<span data-ttu-id="39fc1-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39fc1-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39fc1-113">Área:</span><span class="sxs-lookup"><span data-stu-id="39fc1-113">Area:</span></span>  <br/> |<span data-ttu-id="39fc1-114">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="39fc1-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39fc1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39fc1-115">Remarks</span></span>

<span data-ttu-id="39fc1-116">Al obtener acceso a mensajes de correo electrónico como las conversaciones y la conversión de propiedades del mensaje al [Formato de encapsulación neutro para el transporte (TNEF)](transport-neutral-encapsulation-format-tnef.md), no utilice esta propiedad; en su lugar, use las propiedades [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canónicas.</span><span class="sxs-lookup"><span data-stu-id="39fc1-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="39fc1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="39fc1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39fc1-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="39fc1-118">Protocol specifications</span></span>

<span data-ttu-id="39fc1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39fc1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39fc1-120">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="39fc1-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39fc1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39fc1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39fc1-122">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="39fc1-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="39fc1-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39fc1-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39fc1-124">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="39fc1-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39fc1-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="39fc1-125">Header files</span></span>

<span data-ttu-id="39fc1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39fc1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="39fc1-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="39fc1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="39fc1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39fc1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="39fc1-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="39fc1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39fc1-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="39fc1-130">See also</span></span>



[<span data-ttu-id="39fc1-131">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="39fc1-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="39fc1-132">Carpetas especiales de MAPI</span><span class="sxs-lookup"><span data-stu-id="39fc1-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="39fc1-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="39fc1-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39fc1-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="39fc1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39fc1-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="39fc1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39fc1-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="39fc1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

