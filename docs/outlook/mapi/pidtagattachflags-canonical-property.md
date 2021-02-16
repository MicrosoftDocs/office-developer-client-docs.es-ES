---
title: Propiedad canónica PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339336"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="8060d-103">Propiedad canónica PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="8060d-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8060d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8060d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8060d-105">Contiene una máscara de bits de marcas para datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8060d-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8060d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8060d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8060d-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8060d-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="8060d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8060d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8060d-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="8060d-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="8060d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8060d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8060d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8060d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8060d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8060d-112">Area:</span></span>  <br/> |<span data-ttu-id="8060d-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="8060d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8060d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8060d-114">Remarks</span></span>

<span data-ttu-id="8060d-115">Esta propiedad se usa para la compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="8060d-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="8060d-116">Se pueden establecer una o varias de las siguientes marcas para la **máscara PR_ATTACH_FLAGS** bits:</span><span class="sxs-lookup"><span data-stu-id="8060d-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="8060d-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="8060d-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="8060d-118">Indica que estos datos adjuntos no están disponibles para las aplicaciones de representación HTML y deben omitirse en el procesamiento de extensiones multipropósito de correo de Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="8060d-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="8060d-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="8060d-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="8060d-120">Indica que estos datos adjuntos no están disponibles para las aplicaciones que se representa en formato de texto enriquecido (RTF) y deben omitirse mediante MAPI.</span><span class="sxs-lookup"><span data-stu-id="8060d-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="8060d-121">Si la **PR_ATTACH_FLAGS** es cero o no está presente, todas las aplicaciones procesarán los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8060d-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8060d-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8060d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8060d-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8060d-123">Protocol specifications</span></span>

<span data-ttu-id="8060d-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8060d-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8060d-125">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8060d-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8060d-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8060d-126">Header files</span></span>

<span data-ttu-id="8060d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8060d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8060d-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8060d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8060d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8060d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8060d-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8060d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8060d-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8060d-131">See also</span></span>



[<span data-ttu-id="8060d-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8060d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8060d-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8060d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8060d-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8060d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8060d-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8060d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

