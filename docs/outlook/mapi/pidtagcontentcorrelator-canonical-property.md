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
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438529"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="9defc-103">Propiedad canónica PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="9defc-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="9defc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9defc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9defc-105">Contiene un valor que el remitente del mensaje puede usar para hacer coincidir un informe con el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="9defc-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9defc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9defc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9defc-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="9defc-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="9defc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9defc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9defc-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="9defc-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="9defc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9defc-110">Data type:</span></span>  <br/> |<span data-ttu-id="9defc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9defc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9defc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9defc-112">Area:</span></span>  <br/> |<span data-ttu-id="9defc-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="9defc-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9defc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9defc-114">Remarks</span></span>

<span data-ttu-id="9defc-115">El originador del mensaje define el contenido de la cadena binaria.</span><span class="sxs-lookup"><span data-stu-id="9defc-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="9defc-116">Si se establece en un mensaje saliente, esta propiedad debe copiarse en los informes generados en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="9defc-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9defc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9defc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9defc-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9defc-118">Header files</span></span>

<span data-ttu-id="9defc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9defc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9defc-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9defc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9defc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9defc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9defc-122">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9defc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9defc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9defc-123">See also</span></span>



[<span data-ttu-id="9defc-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9defc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9defc-125">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9defc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9defc-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9defc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9defc-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9defc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

