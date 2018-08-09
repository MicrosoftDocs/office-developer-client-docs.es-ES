---
title: Propiedad canónica PidLidImageAttachmentsCompressionLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818755"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="ae8ce-103">Propiedad canónica PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="ae8ce-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="ae8ce-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae8ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae8ce-105">Define un nivel de compresión que se debe aplicar en datos adjuntos de imágenes.</span><span class="sxs-lookup"><span data-stu-id="ae8ce-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae8ce-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ae8ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae8ce-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="ae8ce-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="ae8ce-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ae8ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="ae8ce-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ae8ce-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ae8ce-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="ae8ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ae8ce-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="ae8ce-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="ae8ce-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ae8ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="ae8ce-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ae8ce-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ae8ce-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ae8ce-114">Area:</span></span>  <br/> |<span data-ttu-id="ae8ce-115">Configuración de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ae8ce-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae8ce-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae8ce-116">Remarks</span></span>

<span data-ttu-id="ae8ce-117">Los siguientes son los niveles de compresión válidos:</span><span class="sxs-lookup"><span data-stu-id="ae8ce-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="ae8ce-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae8ce-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae8ce-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ae8ce-119">Protocol specifications</span></span>

<span data-ttu-id="ae8ce-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="ae8ce-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="ae8ce-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ae8ce-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae8ce-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ae8ce-122">Header files</span></span>

<span data-ttu-id="ae8ce-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae8ce-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae8ce-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ae8ce-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae8ce-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae8ce-125">See also</span></span>



[<span data-ttu-id="ae8ce-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ae8ce-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae8ce-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ae8ce-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae8ce-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ae8ce-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae8ce-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ae8ce-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

