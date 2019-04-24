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
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357585"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="6a41a-103">Propiedad canónica PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="6a41a-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="6a41a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a41a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a41a-105">Define el nivel de compresión que se debe aplicar en los datos adjuntos de imagen.</span><span class="sxs-lookup"><span data-stu-id="6a41a-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a41a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6a41a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a41a-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="6a41a-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="6a41a-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6a41a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a41a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6a41a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6a41a-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="6a41a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6a41a-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="6a41a-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="6a41a-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6a41a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a41a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6a41a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6a41a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6a41a-114">Area:</span></span>  <br/> |<span data-ttu-id="6a41a-115">Configuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="6a41a-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a41a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a41a-116">Remarks</span></span>

<span data-ttu-id="6a41a-117">Los siguientes niveles de compresión son válidos:</span><span class="sxs-lookup"><span data-stu-id="6a41a-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="6a41a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a41a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a41a-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6a41a-119">Protocol specifications</span></span>

<span data-ttu-id="6a41a-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="6a41a-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="6a41a-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6a41a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a41a-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6a41a-122">Header files</span></span>

<span data-ttu-id="6a41a-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6a41a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a41a-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6a41a-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a41a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a41a-125">See also</span></span>



[<span data-ttu-id="6a41a-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6a41a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a41a-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="6a41a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a41a-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6a41a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a41a-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6a41a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

