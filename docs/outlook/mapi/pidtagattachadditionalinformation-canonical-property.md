---
title: Propiedad canónica PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819208"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="1e753-103">Propiedad canónica PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="1e753-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="1e753-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e753-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e753-105">Proporciona información de tipo de archivo para datos adjuntos de que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="1e753-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e753-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1e753-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e753-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="1e753-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="1e753-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1e753-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e753-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="1e753-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="1e753-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1e753-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e753-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e753-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e753-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1e753-112">Area:</span></span>  <br/> |<span data-ttu-id="1e753-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="1e753-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e753-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e753-114">Remarks</span></span>

<span data-ttu-id="1e753-115">Esta propiedad proporciona metadatos sobre un dato adjunto determinado en función de la codificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1e753-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="1e753-116">Por ejemplo, cuando la propiedad **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contiene MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contiene una cadena que representa el tipo de archivo, con formato como ":CREA:TYPE" y creador de archivo de Macintosh para el archivo codificado de Macintosh.</span><span class="sxs-lookup"><span data-stu-id="1e753-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e753-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e753-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e753-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1e753-118">Protocol specifications</span></span>

<span data-ttu-id="1e753-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e753-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e753-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1e753-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e753-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1e753-121">Header files</span></span>

<span data-ttu-id="1e753-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e753-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e753-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1e753-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e753-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e753-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1e753-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1e753-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e753-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e753-126">See also</span></span>



[<span data-ttu-id="1e753-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e753-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e753-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1e753-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e753-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1e753-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e753-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1e753-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

