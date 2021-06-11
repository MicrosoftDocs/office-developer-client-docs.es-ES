---
title: Propiedad canónica PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359048"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="ddd63-103">Propiedad canónica PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="ddd63-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="ddd63-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddd63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddd63-105">Contiene la versión del lenguaje de marcado de hipertexto (HTML) del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddd63-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddd63-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ddd63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ddd63-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="ddd63-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="ddd63-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ddd63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ddd63-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="ddd63-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="ddd63-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ddd63-110">Data type:</span></span>  <br/> |<span data-ttu-id="ddd63-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ddd63-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ddd63-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ddd63-112">Area:</span></span>  <br/> |<span data-ttu-id="ddd63-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="ddd63-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddd63-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddd63-114">Remarks</span></span>

<span data-ttu-id="ddd63-115">Estas propiedades contienen el mismo texto de mensaje que **el PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), pero en HTML.</span><span class="sxs-lookup"><span data-stu-id="ddd63-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="ddd63-116">Un almacén de mensajes que admite HTML indica esto estableciendo la marca **STORE_HTML_OK** en su PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ddd63-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="ddd63-117">**Nota** **STORE_HTML_OK** no se define en las versiones de Mapidefs.h incluidas con Microsoft® Exchange 2000 Server y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ddd63-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="ddd63-118">Si **STORE_HTML_OK** no está definido, use el valor 0x00010000 su lugar.</span><span class="sxs-lookup"><span data-stu-id="ddd63-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ddd63-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddd63-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ddd63-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ddd63-120">Protocol specifications</span></span>

<span data-ttu-id="ddd63-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddd63-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddd63-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ddd63-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ddd63-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddd63-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddd63-124">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ddd63-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ddd63-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ddd63-125">Header files</span></span>

<span data-ttu-id="ddd63-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ddd63-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddd63-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ddd63-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ddd63-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ddd63-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ddd63-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ddd63-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddd63-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddd63-130">See also</span></span>



[<span data-ttu-id="ddd63-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd63-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddd63-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd63-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddd63-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd63-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddd63-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ddd63-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

