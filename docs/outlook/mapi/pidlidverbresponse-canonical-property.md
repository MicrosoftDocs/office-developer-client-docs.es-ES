---
title: Propiedad canónica PidLidVerbResponse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidVerbResponse
api_type:
- COM
ms.assetid: 6f3db5ac-f1cb-4c55-ab88-c126dd5f48ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 267fcc2b6f8902b1f9abb7adcd4409875fc1a7b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819032"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="3a63b-103">Propiedad canónica PidLidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="3a63b-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="3a63b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a63b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a63b-105">Especifica la opción de votación que cuestionario seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3a63b-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a63b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3a63b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a63b-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="3a63b-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="3a63b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3a63b-108">Property set:</span></span>  <br/> |<span data-ttu-id="3a63b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3a63b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3a63b-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="3a63b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3a63b-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="3a63b-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="3a63b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3a63b-112">Data type:</span></span>  <br/> |<span data-ttu-id="3a63b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a63b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3a63b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3a63b-114">Area:</span></span>  <br/> |<span data-ttu-id="3a63b-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="3a63b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a63b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a63b-116">Remarks</span></span>

<span data-ttu-id="3a63b-117">Normalmente, esta propiedad se establece en uno de los valores delimitados que están contenidos en la propiedad **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) en el que se aprueba el demandado.</span><span class="sxs-lookup"><span data-stu-id="3a63b-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a63b-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a63b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a63b-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3a63b-119">Protocol specifications</span></span>

<span data-ttu-id="3a63b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a63b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a63b-121">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3a63b-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a63b-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a63b-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a63b-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3a63b-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a63b-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3a63b-124">Header files</span></span>

<span data-ttu-id="3a63b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a63b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a63b-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3a63b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a63b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a63b-127">See also</span></span>



[<span data-ttu-id="3a63b-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3a63b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a63b-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3a63b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a63b-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3a63b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a63b-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3a63b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

