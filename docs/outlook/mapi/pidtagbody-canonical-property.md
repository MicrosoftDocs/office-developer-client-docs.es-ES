---
title: Propiedad canónica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819265"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="d6eb4-103">Propiedad canónica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="d6eb4-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="d6eb4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6eb4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6eb4-105">Contiene el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6eb4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6eb4-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="d6eb4-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="d6eb4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6eb4-109">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="d6eb4-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="d6eb4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6eb4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d6eb4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d6eb4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6eb4-112">Area:</span></span>  <br/> |<span data-ttu-id="d6eb4-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="d6eb4-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6eb4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6eb4-114">Remarks</span></span>

<span data-ttu-id="d6eb4-115">Estas propiedades se suelen usar sólo en un mensaje interpersonal (IPM).</span><span class="sxs-lookup"><span data-stu-id="d6eb4-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="d6eb4-116">Almacenes de mensaje que admiten el formato de texto enriquecido (RTF) omitir los cambios realizados en el espacio en blanco en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="d6eb4-117">Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la versión RTF del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="d6eb4-118">Si posteriormente se llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y **PR_BODY** se ha modificado, el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión RTF.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="d6eb4-119">Si sólo se ha cambiado el espacio en blanco, las propiedades se dejan sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="d6eb4-120">Esto significa que mantiene cualquier RTF no trivial formato cuando el mensaje se transmite a través de clientes ajenos a RTF y sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="d6eb4-121">El valor de esta propiedad debe expresarse en la página de códigos del sistema operativo que se está ejecutando MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6eb4-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6eb4-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6eb4-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6eb4-123">Protocol specifications</span></span>

<span data-ttu-id="d6eb4-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6eb4-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6eb4-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6eb4-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6eb4-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6eb4-127">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6eb4-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d6eb4-128">Header files</span></span>

<span data-ttu-id="d6eb4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6eb4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6eb4-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6eb4-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6eb4-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d6eb4-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d6eb4-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6eb4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6eb4-133">See also</span></span>



[<span data-ttu-id="d6eb4-134">Propiedad canónica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="d6eb4-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="d6eb4-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6eb4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6eb4-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d6eb4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6eb4-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d6eb4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6eb4-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d6eb4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

