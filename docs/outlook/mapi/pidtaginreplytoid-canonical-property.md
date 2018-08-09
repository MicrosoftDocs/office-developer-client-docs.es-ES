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
ms.openlocfilehash: 2e8ed4af81de6e48af3e427f2d2d2f94572d241f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819611"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="0dc1f-103">Propiedad canónica PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="0dc1f-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="0dc1f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0dc1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0dc1f-105">Contiene el valor de la propiedad **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0dc1f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0dc1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dc1f-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="0dc1f-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="0dc1f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0dc1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dc1f-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="0dc1f-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="0dc1f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0dc1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dc1f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0dc1f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0dc1f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0dc1f-112">Area:</span></span>  <br/> |<span data-ttu-id="0dc1f-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="0dc1f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dc1f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0dc1f-114">Remarks</span></span>

<span data-ttu-id="0dc1f-115">Estas propiedades se deben establecer en todas las respuestas de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0dc1f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0dc1f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dc1f-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0dc1f-117">Protocol specifications</span></span>

<span data-ttu-id="0dc1f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dc1f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dc1f-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dc1f-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dc1f-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dc1f-121">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="0dc1f-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dc1f-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dc1f-123">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dc1f-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0dc1f-124">Header files</span></span>

<span data-ttu-id="0dc1f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dc1f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dc1f-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dc1f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0dc1f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0dc1f-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dc1f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dc1f-129">See also</span></span>



[<span data-ttu-id="0dc1f-130">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="0dc1f-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="0dc1f-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0dc1f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dc1f-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0dc1f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dc1f-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0dc1f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dc1f-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0dc1f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

