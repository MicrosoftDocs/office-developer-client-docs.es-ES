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
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359919"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="0f235-103">Propiedad canónica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="0f235-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="0f235-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f235-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f235-105">Contiene TRUE si una aplicación cliente desea que MAPI elimine el mensaje asociado después del envío.</span><span class="sxs-lookup"><span data-stu-id="0f235-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f235-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0f235-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f235-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0f235-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="0f235-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0f235-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f235-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="0f235-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="0f235-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0f235-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f235-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0f235-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0f235-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0f235-112">Area:</span></span>  <br/> |<span data-ttu-id="0f235-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="0f235-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f235-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f235-114">Remarks</span></span>

<span data-ttu-id="0f235-115">Una aplicación cliente usa esta propiedad con la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para controlar lo que sucede con un mensaje después de que se envía.</span><span class="sxs-lookup"><span data-stu-id="0f235-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="0f235-116">Uno u otro deben establecerse, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="0f235-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f235-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f235-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f235-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0f235-118">Protocol specifications</span></span>

<span data-ttu-id="0f235-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f235-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f235-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0f235-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f235-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f235-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f235-122">Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f235-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="0f235-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f235-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f235-124">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0f235-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f235-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0f235-125">Header files</span></span>

<span data-ttu-id="0f235-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f235-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f235-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0f235-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f235-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f235-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0f235-129">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="0f235-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f235-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0f235-130">See also</span></span>



[<span data-ttu-id="0f235-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0f235-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f235-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0f235-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f235-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0f235-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f235-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0f235-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

