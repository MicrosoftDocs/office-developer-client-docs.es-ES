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
ms.openlocfilehash: 869f7f0bb4ea5e7222201083cb6d41754d241396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820274"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="d4468-103">Propiedad canónica PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="d4468-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d4468-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4468-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4468-105">Contiene el identificador de entrada de la carpeta donde se va a mover el mensaje después de la presentación.</span><span class="sxs-lookup"><span data-stu-id="d4468-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4468-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d4468-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4468-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d4468-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d4468-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4468-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4468-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="d4468-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="d4468-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d4468-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4468-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4468-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4468-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4468-112">Area:</span></span>  <br/> |<span data-ttu-id="d4468-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="d4468-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4468-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4468-114">Remarks</span></span>

<span data-ttu-id="d4468-115">Esta propiedad a menudo se copia desde la propiedad de **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), la carpeta Elementos enviados de estándar de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="d4468-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="d4468-116">La aplicación cliente usa esta propiedad con la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para controlar lo que ocurre con un mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="d4468-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="d4468-117">Debe ser uno u otro conjunto, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="d4468-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4468-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4468-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4468-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d4468-119">Protocol specifications</span></span>

<span data-ttu-id="d4468-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4468-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4468-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d4468-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4468-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4468-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4468-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d4468-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d4468-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4468-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4468-125">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d4468-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4468-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d4468-126">Header files</span></span>

<span data-ttu-id="d4468-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4468-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4468-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d4468-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4468-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4468-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d4468-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d4468-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4468-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4468-131">See also</span></span>



[<span data-ttu-id="d4468-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4468-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4468-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d4468-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4468-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d4468-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4468-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d4468-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

