---
title: Propiedad canónica PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568808"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="41f4b-103">Propiedad canónica PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="41f4b-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="41f4b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41f4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41f4b-105">Contiene un valor que se puede usar el remitente del mensaje para que coincida con un informe con el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="41f4b-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41f4b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="41f4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41f4b-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="41f4b-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="41f4b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="41f4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41f4b-109">0 x 0007</span><span class="sxs-lookup"><span data-stu-id="41f4b-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="41f4b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="41f4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="41f4b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="41f4b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="41f4b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="41f4b-112">Area:</span></span>  <br/> |<span data-ttu-id="41f4b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="41f4b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41f4b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41f4b-114">Remarks</span></span>

<span data-ttu-id="41f4b-115">El contenido de la cadena binaria se define por el autor del mensaje.</span><span class="sxs-lookup"><span data-stu-id="41f4b-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="41f4b-116">Si se configura en un mensaje saliente, esta propiedad debe copiarse en cualquier informes generados en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="41f4b-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41f4b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="41f4b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="41f4b-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="41f4b-118">Header files</span></span>

<span data-ttu-id="41f4b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41f4b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="41f4b-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="41f4b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="41f4b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41f4b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="41f4b-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="41f4b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41f4b-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="41f4b-123">See also</span></span>



[<span data-ttu-id="41f4b-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="41f4b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41f4b-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="41f4b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41f4b-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="41f4b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41f4b-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="41f4b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

