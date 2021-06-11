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
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="56dac-103">Propiedad canónica PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="56dac-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="56dac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56dac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56dac-105">Contiene el encabezado de identificación de contenido de un archivo adjunto de mensaje multipropósito de Extensiones de correo de Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="56dac-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56dac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="56dac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56dac-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="56dac-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="56dac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="56dac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56dac-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="56dac-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="56dac-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="56dac-110">Data type:</span></span>  <br/> |<span data-ttu-id="56dac-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="56dac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="56dac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="56dac-112">Area:</span></span>  <br/> |<span data-ttu-id="56dac-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="56dac-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56dac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56dac-114">Remarks</span></span>

<span data-ttu-id="56dac-115">Estas propiedades se usan para la compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="56dac-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="56dac-116">Representan el encabezado de identificación de contenido de la parte del cuerpo MIME correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56dac-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56dac-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="56dac-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56dac-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="56dac-118">Protocol specifications</span></span>

<span data-ttu-id="56dac-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56dac-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56dac-120">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="56dac-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="56dac-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="56dac-121">Header Files</span></span>

<span data-ttu-id="56dac-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56dac-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="56dac-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="56dac-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="56dac-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56dac-124">Mapitags.h</span></span>
  
> <span data-ttu-id="56dac-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="56dac-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56dac-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="56dac-126">See also</span></span>



[<span data-ttu-id="56dac-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="56dac-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56dac-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="56dac-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56dac-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="56dac-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56dac-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="56dac-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

