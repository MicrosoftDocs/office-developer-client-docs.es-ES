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
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335437"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="106f2-103">Propiedad canónica PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="106f2-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="106f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="106f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="106f2-105">Esta propiedad contiene un número que indica el estado de una transferencia remota.</span><span class="sxs-lookup"><span data-stu-id="106f2-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="106f2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="106f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="106f2-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="106f2-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="106f2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="106f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="106f2-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="106f2-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="106f2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="106f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="106f2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="106f2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="106f2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="106f2-112">Area:</span></span>  <br/> |<span data-ttu-id="106f2-113">Estado de MAPI</span><span class="sxs-lookup"><span data-stu-id="106f2-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="106f2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="106f2-114">Remarks</span></span>

<span data-ttu-id="106f2-115">Si no hay transferencia en curso, esta propiedad debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="106f2-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="106f2-116">Si se está realizando una transferencia, debe establecerse en un valor entre 0 y 100 que indica el porcentaje de finalización de la transferencia.</span><span class="sxs-lookup"><span data-stu-id="106f2-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="106f2-117">El texto asociado con el código de estado numérico aparece en la propiedad **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="106f2-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="106f2-118">Se pueden establecer los siguientes indicadores para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="106f2-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="106f2-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="106f2-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="106f2-120">Se elimina la transferencia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="106f2-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="106f2-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="106f2-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="106f2-122">La transferencia del mensaje está en curso.</span><span class="sxs-lookup"><span data-stu-id="106f2-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="106f2-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="106f2-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="106f2-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="106f2-124">Header files</span></span>

<span data-ttu-id="106f2-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="106f2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="106f2-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="106f2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="106f2-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="106f2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="106f2-128">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="106f2-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="106f2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="106f2-129">See also</span></span>



[<span data-ttu-id="106f2-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="106f2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="106f2-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="106f2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="106f2-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="106f2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="106f2-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="106f2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

