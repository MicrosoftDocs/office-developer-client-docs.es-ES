---
title: Propiedad canónica PidTagAttachContentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5fc7360e3070ed4d20be7ac0155ebdcb04cf2048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319211"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="407e3-103">Propiedad canónica PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="407e3-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="407e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="407e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="407e3-105">Contiene el encabezado de identificación de contenido de los datos adjuntos de un mensaje de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="407e3-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="407e3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="407e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="407e3-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="407e3-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="407e3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="407e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="407e3-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="407e3-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="407e3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="407e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="407e3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="407e3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="407e3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="407e3-112">Area:</span></span>  <br/> |<span data-ttu-id="407e3-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="407e3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="407e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="407e3-114">Remarks</span></span>

<span data-ttu-id="407e3-115">Estas propiedades se usan para la compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="407e3-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="407e3-116">Representan el encabezado de identificación de contenido para la parte del cuerpo MIME correspondiente.</span><span class="sxs-lookup"><span data-stu-id="407e3-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="407e3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="407e3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="407e3-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="407e3-118">Protocol specifications</span></span>

<span data-ttu-id="407e3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="407e3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="407e3-120">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="407e3-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="407e3-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="407e3-121">Header Files</span></span>

<span data-ttu-id="407e3-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="407e3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="407e3-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="407e3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="407e3-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="407e3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="407e3-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="407e3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="407e3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="407e3-126">See also</span></span>



[<span data-ttu-id="407e3-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="407e3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="407e3-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="407e3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="407e3-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="407e3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="407e3-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="407e3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

