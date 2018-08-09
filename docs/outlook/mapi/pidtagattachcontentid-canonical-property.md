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
ms.openlocfilehash: edd0df690df6af47ed6db34dc4a658b24136077c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819226"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="88986-103">Propiedad canónica PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="88986-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="88986-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88986-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88986-105">Contiene el encabezado de identificación de contenido de datos adjuntos de mensajes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="88986-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88986-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="88986-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88986-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="88986-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="88986-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="88986-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88986-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="88986-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="88986-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="88986-110">Data type:</span></span>  <br/> |<span data-ttu-id="88986-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="88986-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="88986-112">Área:</span><span class="sxs-lookup"><span data-stu-id="88986-112">Area:</span></span>  <br/> |<span data-ttu-id="88986-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="88986-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88986-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88986-114">Remarks</span></span>

<span data-ttu-id="88986-115">Estas propiedades se utilizan para ofrecer compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="88986-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="88986-116">Representan el encabezado de identificación de contenido de la parte del cuerpo MIME apropiado.</span><span class="sxs-lookup"><span data-stu-id="88986-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="88986-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="88986-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88986-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="88986-118">Protocol specifications</span></span>

<span data-ttu-id="88986-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88986-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88986-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="88986-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="88986-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="88986-121">Header Files</span></span>

<span data-ttu-id="88986-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88986-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="88986-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="88986-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="88986-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88986-124">Mapitags.h</span></span>
  
> <span data-ttu-id="88986-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="88986-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88986-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="88986-126">See also</span></span>



[<span data-ttu-id="88986-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="88986-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88986-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="88986-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88986-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="88986-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88986-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="88986-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

