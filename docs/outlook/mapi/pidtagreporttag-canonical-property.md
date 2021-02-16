---
title: Propiedad canónica PidTagReportTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331433"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="c84ef-103">Propiedad canónica PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="c84ef-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="c84ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c84ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c84ef-105">Contiene un valor de etiqueta binaria que el sistema de mensajería debe copiar en cualquier informe generado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c84ef-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c84ef-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c84ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c84ef-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="c84ef-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="c84ef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c84ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c84ef-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="c84ef-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="c84ef-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c84ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="c84ef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c84ef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c84ef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c84ef-112">Area:</span></span>  <br/> |<span data-ttu-id="c84ef-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="c84ef-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c84ef-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c84ef-114">Remarks</span></span>

<span data-ttu-id="c84ef-115">Esta propiedad, como **la PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)), se usa para correlacionar un informe con el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="c84ef-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c84ef-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c84ef-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c84ef-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c84ef-117">Protocol specifications</span></span>

<span data-ttu-id="c84ef-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c84ef-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c84ef-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c84ef-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c84ef-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c84ef-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c84ef-121">Especifica las propiedades y operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c84ef-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c84ef-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c84ef-122">Header files</span></span>

<span data-ttu-id="c84ef-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c84ef-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c84ef-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c84ef-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c84ef-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c84ef-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c84ef-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c84ef-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c84ef-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c84ef-127">See also</span></span>



[<span data-ttu-id="c84ef-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c84ef-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c84ef-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c84ef-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c84ef-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c84ef-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c84ef-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c84ef-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

