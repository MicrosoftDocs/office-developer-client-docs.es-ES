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
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571615"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="18c2d-103">Propiedad canónica PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="18c2d-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="18c2d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18c2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18c2d-105">Contiene la fecha y hora que había pasado de un proveedor de transporte de un mensaje a su sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="18c2d-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18c2d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="18c2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18c2d-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="18c2d-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="18c2d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="18c2d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18c2d-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="18c2d-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="18c2d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="18c2d-110">Data type:</span></span>  <br/> |<span data-ttu-id="18c2d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="18c2d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="18c2d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="18c2d-112">Area:</span></span>  <br/> |<span data-ttu-id="18c2d-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="18c2d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18c2d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18c2d-114">Remarks</span></span>

<span data-ttu-id="18c2d-115">Esta propiedad se establece por el proveedor de transporte saliente en el momento en que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="18c2d-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="18c2d-116">Esta propiedad corresponde a un atributo de cada mensaje X.400 envelope de envío.</span><span class="sxs-lookup"><span data-stu-id="18c2d-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="18c2d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="18c2d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="18c2d-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="18c2d-118">Header files</span></span>

<span data-ttu-id="18c2d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18c2d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="18c2d-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="18c2d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="18c2d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18c2d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="18c2d-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="18c2d-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18c2d-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="18c2d-123">See also</span></span>



[<span data-ttu-id="18c2d-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="18c2d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18c2d-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="18c2d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18c2d-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="18c2d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18c2d-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="18c2d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

