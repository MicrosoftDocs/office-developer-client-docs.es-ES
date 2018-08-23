---
title: Propiedad canónica PidTagInReplyToId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f3ae69243da185430836903da9e7b0644c5db90
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594785"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="414a6-103">Propiedad canónica PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="414a6-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="414a6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="414a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="414a6-105">Contiene el valor de la propiedad **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="414a6-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="414a6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="414a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="414a6-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="414a6-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="414a6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="414a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="414a6-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="414a6-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="414a6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="414a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="414a6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="414a6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="414a6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="414a6-112">Area:</span></span>  <br/> |<span data-ttu-id="414a6-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="414a6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="414a6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="414a6-114">Remarks</span></span>

<span data-ttu-id="414a6-115">Estas propiedades se deben establecer en todas las respuestas de mensajes.</span><span class="sxs-lookup"><span data-stu-id="414a6-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="414a6-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="414a6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="414a6-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="414a6-117">Protocol specifications</span></span>

<span data-ttu-id="414a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="414a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="414a6-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="414a6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="414a6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="414a6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="414a6-121">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="414a6-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="414a6-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="414a6-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="414a6-123">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="414a6-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="414a6-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="414a6-124">Header files</span></span>

<span data-ttu-id="414a6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="414a6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="414a6-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="414a6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="414a6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="414a6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="414a6-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="414a6-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="414a6-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="414a6-129">See also</span></span>



[<span data-ttu-id="414a6-130">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="414a6-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="414a6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="414a6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="414a6-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="414a6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="414a6-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="414a6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="414a6-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="414a6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

