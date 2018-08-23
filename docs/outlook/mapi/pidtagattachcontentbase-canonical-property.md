---
title: Propiedad canónica PidTagAttachContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 40e2efbf512265dffeee43d09e85879e8c3a0e56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582423"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="841e5-103">Propiedad canónica PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="841e5-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="841e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="841e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="841e5-105">Contiene el encabezado contenido de base de datos adjuntos de mensajes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="841e5-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="841e5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="841e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="841e5-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="841e5-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="841e5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="841e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="841e5-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="841e5-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="841e5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="841e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="841e5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="841e5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="841e5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="841e5-112">Area:</span></span>  <br/> |<span data-ttu-id="841e5-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="841e5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="841e5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="841e5-114">Remarks</span></span>

<span data-ttu-id="841e5-115">Estas propiedades se utilizan para ofrecer compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="841e5-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="841e5-116">Representan el encabezado de contenido base para la parte del cuerpo MIME apropiado.</span><span class="sxs-lookup"><span data-stu-id="841e5-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="841e5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="841e5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="841e5-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="841e5-118">Protocol specifications</span></span>

<span data-ttu-id="841e5-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="841e5-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="841e5-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="841e5-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="841e5-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="841e5-121">Header files</span></span>

<span data-ttu-id="841e5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="841e5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="841e5-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="841e5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="841e5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="841e5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="841e5-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="841e5-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="841e5-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="841e5-126">See also</span></span>



[<span data-ttu-id="841e5-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="841e5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="841e5-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="841e5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="841e5-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="841e5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="841e5-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="841e5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

