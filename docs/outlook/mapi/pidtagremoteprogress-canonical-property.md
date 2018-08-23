---
title: Propiedad canónica PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569354"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="323b0-103">Propiedad canónica PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="323b0-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="323b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="323b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="323b0-105">Esta propiedad contiene un número que indica el estado de una transferencia remota.</span><span class="sxs-lookup"><span data-stu-id="323b0-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="323b0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="323b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="323b0-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="323b0-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="323b0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="323b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="323b0-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="323b0-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="323b0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="323b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="323b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="323b0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="323b0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="323b0-112">Area:</span></span>  <br/> |<span data-ttu-id="323b0-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="323b0-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="323b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="323b0-114">Remarks</span></span>

<span data-ttu-id="323b0-115">Si no hay transferencia está en curso, esta propiedad debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="323b0-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="323b0-116">Si hay una transferencia en curso, debe establecerse en un valor de 0 a 100 que indica el porcentaje de la transferencia de finalización.</span><span class="sxs-lookup"><span data-stu-id="323b0-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="323b0-117">El texto asociado con el código de estado numérico aparece en la propiedad **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="323b0-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="323b0-118">Para esta propiedad se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="323b0-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="323b0-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="323b0-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="323b0-120">Se elimina la transferencia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="323b0-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="323b0-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="323b0-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="323b0-122">La transferencia del mensaje está en curso.</span><span class="sxs-lookup"><span data-stu-id="323b0-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="323b0-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="323b0-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="323b0-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="323b0-124">Header files</span></span>

<span data-ttu-id="323b0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="323b0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="323b0-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="323b0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="323b0-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="323b0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="323b0-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="323b0-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="323b0-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="323b0-129">See also</span></span>



[<span data-ttu-id="323b0-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="323b0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="323b0-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="323b0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="323b0-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="323b0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="323b0-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="323b0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

