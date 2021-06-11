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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345482"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="f4b6b-103">Propiedad canónica PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="f4b6b-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="f4b6b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4b6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4b6b-105">Contiene el encabezado de ubicación de contenido de un archivo adjunto de mensaje Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="f4b6b-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4b6b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f4b6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4b6b-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="f4b6b-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="f4b6b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f4b6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4b6b-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="f4b6b-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="f4b6b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f4b6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4b6b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4b6b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4b6b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f4b6b-112">Area:</span></span>  <br/> |<span data-ttu-id="f4b6b-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="f4b6b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4b6b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4b6b-114">Remarks</span></span>

<span data-ttu-id="f4b6b-115">Estas propiedades se usan para la compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="f4b6b-116">Representan el encabezado de ubicación de contenido de la parte del cuerpo MIME correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4b6b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4b6b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4b6b-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f4b6b-118">Protocol specifications</span></span>

<span data-ttu-id="f4b6b-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4b6b-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4b6b-120">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4b6b-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f4b6b-121">Header files</span></span>

<span data-ttu-id="f4b6b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4b6b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4b6b-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4b6b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4b6b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f4b6b-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4b6b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4b6b-126">See also</span></span>



[<span data-ttu-id="f4b6b-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4b6b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4b6b-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f4b6b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4b6b-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f4b6b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4b6b-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f4b6b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

