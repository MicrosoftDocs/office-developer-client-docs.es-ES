---
title: Propiedad canónica PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b53275d3bf26aa8bee3aeaef2148f5ead961e471
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591656"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="73af3-103">Propiedad canónica PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="73af3-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="73af3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73af3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73af3-105">Contiene el identificador de entrada de la carpeta donde se va a mover el mensaje después de la presentación.</span><span class="sxs-lookup"><span data-stu-id="73af3-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73af3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="73af3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73af3-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="73af3-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="73af3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="73af3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73af3-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="73af3-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="73af3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="73af3-110">Data type:</span></span>  <br/> |<span data-ttu-id="73af3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73af3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73af3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="73af3-112">Area:</span></span>  <br/> |<span data-ttu-id="73af3-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="73af3-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73af3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73af3-114">Remarks</span></span>

<span data-ttu-id="73af3-115">Esta propiedad a menudo se copia desde la propiedad de **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), la carpeta Elementos enviados de estándar de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="73af3-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="73af3-116">La aplicación cliente usa esta propiedad con la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para controlar lo que ocurre con un mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="73af3-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="73af3-117">Debe ser uno u otro conjunto, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="73af3-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73af3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="73af3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73af3-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="73af3-119">Protocol specifications</span></span>

<span data-ttu-id="73af3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73af3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73af3-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="73af3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73af3-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73af3-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73af3-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="73af3-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="73af3-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73af3-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73af3-125">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="73af3-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73af3-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="73af3-126">Header files</span></span>

<span data-ttu-id="73af3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73af3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="73af3-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="73af3-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="73af3-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73af3-129">Mapitags.h</span></span>
  
> <span data-ttu-id="73af3-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="73af3-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73af3-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="73af3-131">See also</span></span>



[<span data-ttu-id="73af3-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="73af3-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73af3-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="73af3-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73af3-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="73af3-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73af3-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="73af3-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

