---
title: Propiedad canónica PidTagDeleteAfterSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 21bbb498eb4d53704c7a1a1a5bc84e9c72a75258
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566432"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="1c979-103">Propiedad canónica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="1c979-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="1c979-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c979-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c979-105">Contiene TRUE si desea que una aplicación cliente MAPI para eliminar el mensaje asociado después de la presentación.</span><span class="sxs-lookup"><span data-stu-id="1c979-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c979-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c979-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c979-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="1c979-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="1c979-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c979-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c979-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="1c979-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="1c979-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c979-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c979-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1c979-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1c979-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c979-112">Area:</span></span>  <br/> |<span data-ttu-id="1c979-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="1c979-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c979-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c979-114">Remarks</span></span>

<span data-ttu-id="1c979-115">Una aplicación cliente usa esta propiedad con la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para controlar lo que ocurre con un mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="1c979-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="1c979-116">Debe ser uno u otro conjunto, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="1c979-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c979-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c979-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c979-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1c979-118">Protocol specifications</span></span>

<span data-ttu-id="1c979-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c979-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c979-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1c979-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c979-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c979-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c979-122">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="1c979-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="1c979-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c979-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c979-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1c979-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c979-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c979-125">Header files</span></span>

<span data-ttu-id="1c979-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c979-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c979-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c979-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c979-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c979-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1c979-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="1c979-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c979-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1c979-130">See also</span></span>



[<span data-ttu-id="1c979-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c979-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c979-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1c979-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c979-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1c979-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c979-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1c979-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

