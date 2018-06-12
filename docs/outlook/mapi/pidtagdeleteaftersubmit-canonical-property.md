---
title: Propiedad canónico PidTagDeleteAfterSubmit
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7a63b3ad3c45790e043e1ea8e7d996c4847ef8d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819418"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="627d3-103">Propiedad canónico PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="627d3-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="627d3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="627d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="627d3-105">Contiene TRUE si desea que una aplicación cliente MAPI para eliminar el mensaje asociado después de la presentación.</span><span class="sxs-lookup"><span data-stu-id="627d3-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="627d3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="627d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="627d3-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="627d3-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="627d3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="627d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="627d3-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="627d3-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="627d3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="627d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="627d3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="627d3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="627d3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="627d3-112">Area:</span></span>  <br/> |<span data-ttu-id="627d3-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="627d3-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="627d3-114">Notas</span><span class="sxs-lookup"><span data-stu-id="627d3-114">Remarks</span></span>

<span data-ttu-id="627d3-115">Una aplicación cliente usa esta propiedad con la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para controlar lo que ocurre con un mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="627d3-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="627d3-116">Debe ser uno u otro conjunto, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="627d3-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="627d3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="627d3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="627d3-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="627d3-118">Protocol specifications</span></span>

<span data-ttu-id="627d3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="627d3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="627d3-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="627d3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="627d3-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="627d3-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="627d3-122">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="627d3-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="627d3-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="627d3-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="627d3-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="627d3-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="627d3-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="627d3-125">Header files</span></span>

<span data-ttu-id="627d3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="627d3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="627d3-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="627d3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="627d3-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="627d3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="627d3-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="627d3-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="627d3-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="627d3-130">See also</span></span>



[<span data-ttu-id="627d3-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="627d3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="627d3-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="627d3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="627d3-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="627d3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="627d3-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="627d3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

