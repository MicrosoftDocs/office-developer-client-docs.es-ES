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
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358838"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="ad47b-103">Propiedad canónica PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="ad47b-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="ad47b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad47b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad47b-105">Contiene el valor de la propiedad **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="ad47b-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad47b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ad47b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad47b-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="ad47b-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="ad47b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad47b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad47b-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="ad47b-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="ad47b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ad47b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad47b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad47b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ad47b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad47b-112">Area:</span></span>  <br/> |<span data-ttu-id="ad47b-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="ad47b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad47b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad47b-114">Remarks</span></span>

<span data-ttu-id="ad47b-115">Estas propiedades deben establecerse en todas las respuestas a mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad47b-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad47b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad47b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad47b-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ad47b-117">Protocol specifications</span></span>

<span data-ttu-id="ad47b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad47b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad47b-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ad47b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad47b-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad47b-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad47b-121">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad47b-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="ad47b-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad47b-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad47b-123">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad47b-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad47b-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ad47b-124">Header files</span></span>

<span data-ttu-id="ad47b-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ad47b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad47b-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ad47b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad47b-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ad47b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ad47b-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ad47b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad47b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad47b-129">See also</span></span>



[<span data-ttu-id="ad47b-130">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="ad47b-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="ad47b-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad47b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad47b-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ad47b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad47b-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ad47b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad47b-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ad47b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

