---
title: Propiedad canónica PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820084"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="5a229-103">Propiedad canónica PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="5a229-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="5a229-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a229-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a229-105">Contiene una matriz de tamaño de los identificadores de entrada para los destinatarios que van a obtener una respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a229-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a229-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a229-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a229-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="5a229-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="5a229-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a229-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a229-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="5a229-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="5a229-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a229-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a229-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a229-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a229-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a229-112">Area:</span></span>  <br/> |<span data-ttu-id="5a229-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a229-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a229-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a229-114">Remarks</span></span>

<span data-ttu-id="5a229-115">Esta propiedad contiene una estructura [FLATENTRYLIST](flatentrylist.md) y no es una propiedad multivalor.</span><span class="sxs-lookup"><span data-stu-id="5a229-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="5a229-116">Cuando esta propiedad no está presente, se envía una respuesta sólo para el usuario identificado por la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5a229-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5a229-117">Cuando se definen propiedades **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) y esto, la respuesta se envía a todos los destinatarios identificados por estas dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a229-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="5a229-118">Un proveedor de transporte usa estas propiedades para invalidar la lógica de respuesta habitual.</span><span class="sxs-lookup"><span data-stu-id="5a229-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="5a229-119">Si se establece esta propiedad o la propiedad **PR_REPLY_RECIPIENT_NAMES** , también debe establecerse la propiedad de otra.</span><span class="sxs-lookup"><span data-stu-id="5a229-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="5a229-120">Estas propiedades deben contener el mismo número de destinatarios y que deben contienen en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="5a229-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="5a229-121">Error al tener en cuenta estos requisitos puede generar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="5a229-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a229-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a229-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a229-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5a229-123">Protocol specifications</span></span>

<span data-ttu-id="5a229-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a229-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a229-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5a229-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a229-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a229-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a229-127">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5a229-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="5a229-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a229-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a229-129">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a229-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a229-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a229-130">Header files</span></span>

<span data-ttu-id="5a229-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a229-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a229-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a229-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a229-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a229-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5a229-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5a229-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a229-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a229-135">See also</span></span>



[<span data-ttu-id="5a229-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a229-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a229-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5a229-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a229-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a229-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a229-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5a229-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

