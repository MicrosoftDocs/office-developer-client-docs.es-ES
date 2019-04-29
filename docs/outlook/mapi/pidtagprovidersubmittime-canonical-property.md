---
title: Propiedad canónica PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409023"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="5ed98-103">Propiedad canónica PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="5ed98-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="5ed98-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ed98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ed98-105">Contiene la fecha y la hora en que un proveedor de transporte pasó un mensaje a su sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="5ed98-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ed98-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5ed98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ed98-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="5ed98-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="5ed98-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5ed98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ed98-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="5ed98-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="5ed98-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5ed98-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ed98-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5ed98-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5ed98-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5ed98-112">Area:</span></span>  <br/> |<span data-ttu-id="5ed98-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="5ed98-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ed98-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ed98-114">Remarks</span></span>

<span data-ttu-id="5ed98-115">El proveedor de transporte de salida establece esta propiedad en el momento en que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5ed98-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="5ed98-116">Esta propiedad corresponde a un sobre de envío X. 400 por atributo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5ed98-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ed98-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed98-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ed98-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5ed98-118">Header files</span></span>

<span data-ttu-id="5ed98-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5ed98-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ed98-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5ed98-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ed98-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5ed98-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5ed98-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5ed98-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ed98-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="5ed98-123">See also</span></span>



[<span data-ttu-id="5ed98-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5ed98-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ed98-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5ed98-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ed98-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5ed98-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ed98-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5ed98-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

