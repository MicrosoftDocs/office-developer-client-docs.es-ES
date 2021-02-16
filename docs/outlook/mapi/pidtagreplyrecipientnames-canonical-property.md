---
title: Propiedad canónica PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355177"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="9f330-103">Propiedad canónica PidTagReplyRecipientNames</span><span class="sxs-lookup"><span data-stu-id="9f330-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="9f330-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f330-105">Contiene una lista de nombres para mostrar para los destinatarios que van a obtener una respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f330-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f330-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f330-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f330-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="9f330-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="9f330-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f330-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f330-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="9f330-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="9f330-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f330-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f330-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f330-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9f330-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f330-112">Area:</span></span>  <br/> |<span data-ttu-id="9f330-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="9f330-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f330-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f330-114">Remarks</span></span>

<span data-ttu-id="9f330-115">Estas propiedades contienen los nombres para mostrar separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="9f330-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="9f330-116">Cuando esta propiedad no está presente, solo se envía una respuesta al usuario identificado por la propiedad **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9f330-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="9f330-117">Cuando **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y estas propiedades se definen, la respuesta se envía a todos los destinatarios identificados por estas dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f330-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="9f330-118">Un proveedor de transporte usa estas propiedades para invalidar la lógica de respuesta habitual.</span><span class="sxs-lookup"><span data-stu-id="9f330-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="9f330-119">Si se **PR_REPLY_RECIPIENT_ENTRIES** o estas propiedades, también se debe establecer la otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f330-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="9f330-120">Estas propiedades deben contener el mismo número de destinatarios y deben contenerlas en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="9f330-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="9f330-121">Si no se cumplen estos requisitos, se pueden producir resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="9f330-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9f330-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f330-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f330-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9f330-123">Protocol specifications</span></span>

<span data-ttu-id="9f330-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f330-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f330-125">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9f330-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f330-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f330-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f330-127">Especifica las propiedades y operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9f330-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="9f330-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f330-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f330-129">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f330-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f330-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f330-130">Header files</span></span>

<span data-ttu-id="9f330-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f330-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f330-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f330-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f330-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f330-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9f330-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9f330-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f330-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f330-135">See also</span></span>



[<span data-ttu-id="9f330-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f330-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f330-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f330-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f330-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9f330-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f330-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9f330-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

