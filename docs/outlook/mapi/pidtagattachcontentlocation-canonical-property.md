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
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390138"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="c2989-103">Propiedad canónica PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="c2989-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="c2989-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2989-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2989-105">Contiene el encabezado de ubicación de contenido de datos adjuntos de mensajes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="c2989-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2989-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c2989-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2989-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="c2989-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="c2989-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c2989-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2989-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="c2989-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="c2989-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c2989-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2989-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c2989-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c2989-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c2989-112">Area:</span></span>  <br/> |<span data-ttu-id="c2989-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="c2989-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2989-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2989-114">Remarks</span></span>

<span data-ttu-id="c2989-115">Estas propiedades se utilizan para ofrecer compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="c2989-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="c2989-116">Representan el encabezado de ubicación de contenido de la parte del cuerpo MIME apropiado.</span><span class="sxs-lookup"><span data-stu-id="c2989-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c2989-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2989-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2989-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c2989-118">Protocol specifications</span></span>

<span data-ttu-id="c2989-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2989-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2989-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c2989-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2989-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c2989-121">Header files</span></span>

<span data-ttu-id="c2989-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2989-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2989-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c2989-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2989-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2989-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c2989-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c2989-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2989-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2989-126">See also</span></span>



[<span data-ttu-id="c2989-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c2989-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2989-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c2989-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2989-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c2989-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2989-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c2989-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

