---
title: Propiedad canónica PidTagAttachContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594771"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="759a7-103">Propiedad canónica PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="759a7-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="759a7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="759a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="759a7-105">Contiene el encabezado de ubicación de contenido de datos adjuntos de mensajes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="759a7-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="759a7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="759a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="759a7-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="759a7-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="759a7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="759a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="759a7-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="759a7-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="759a7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="759a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="759a7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="759a7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="759a7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="759a7-112">Area:</span></span>  <br/> |<span data-ttu-id="759a7-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="759a7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="759a7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="759a7-114">Remarks</span></span>

<span data-ttu-id="759a7-115">Estas propiedades se utilizan para ofrecer compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="759a7-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="759a7-116">Representan el encabezado de ubicación de contenido de la parte del cuerpo MIME apropiado.</span><span class="sxs-lookup"><span data-stu-id="759a7-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="759a7-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="759a7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="759a7-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="759a7-118">Protocol specifications</span></span>

<span data-ttu-id="759a7-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="759a7-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="759a7-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="759a7-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="759a7-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="759a7-121">Header files</span></span>

<span data-ttu-id="759a7-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="759a7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="759a7-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="759a7-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="759a7-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="759a7-124">Mapitags.h</span></span>
  
> <span data-ttu-id="759a7-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="759a7-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="759a7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="759a7-126">See also</span></span>



[<span data-ttu-id="759a7-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="759a7-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="759a7-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="759a7-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="759a7-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="759a7-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="759a7-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="759a7-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

