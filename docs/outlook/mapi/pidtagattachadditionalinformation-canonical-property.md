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
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389634"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="34f3c-103">Propiedad canónica PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="34f3c-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="34f3c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34f3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34f3c-105">Proporciona información de tipo de archivo para datos adjuntos de que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="34f3c-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34f3c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="34f3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34f3c-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="34f3c-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="34f3c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="34f3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34f3c-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="34f3c-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="34f3c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="34f3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="34f3c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="34f3c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="34f3c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="34f3c-112">Area:</span></span>  <br/> |<span data-ttu-id="34f3c-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="34f3c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34f3c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34f3c-114">Remarks</span></span>

<span data-ttu-id="34f3c-115">Esta propiedad proporciona metadatos sobre un dato adjunto determinado en función de la codificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="34f3c-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="34f3c-116">Por ejemplo, cuando la propiedad **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contiene MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contiene una cadena que representa el tipo de archivo, con formato como ":CREA:TYPE" y creador de archivo de Macintosh para el archivo codificado de Macintosh.</span><span class="sxs-lookup"><span data-stu-id="34f3c-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="34f3c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="34f3c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34f3c-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="34f3c-118">Protocol specifications</span></span>

<span data-ttu-id="34f3c-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34f3c-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34f3c-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="34f3c-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34f3c-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="34f3c-121">Header files</span></span>

<span data-ttu-id="34f3c-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34f3c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="34f3c-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="34f3c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="34f3c-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34f3c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="34f3c-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="34f3c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34f3c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="34f3c-126">See also</span></span>



[<span data-ttu-id="34f3c-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="34f3c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34f3c-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="34f3c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34f3c-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="34f3c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34f3c-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="34f3c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

