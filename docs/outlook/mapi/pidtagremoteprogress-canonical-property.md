---
title: Propiedad canónico PidTagRemoteProgress
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820070"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="d606d-103">Propiedad canónico PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="d606d-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="d606d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d606d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d606d-105">Esta propiedad contiene un número que indica el estado de una transferencia remota.</span><span class="sxs-lookup"><span data-stu-id="d606d-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d606d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d606d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d606d-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="d606d-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="d606d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d606d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d606d-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="d606d-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="d606d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d606d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d606d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d606d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d606d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d606d-112">Area:</span></span>  <br/> |<span data-ttu-id="d606d-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="d606d-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d606d-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d606d-114">Remarks</span></span>

<span data-ttu-id="d606d-115">Si no hay transferencia está en curso, esta propiedad debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="d606d-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="d606d-116">Si hay una transferencia en curso, debe establecerse en un valor de 0 a 100 que indica el porcentaje de la transferencia de finalización.</span><span class="sxs-lookup"><span data-stu-id="d606d-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="d606d-117">El texto asociado con el código de estado numérico aparece en la propiedad **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d606d-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d606d-118">Para esta propiedad se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d606d-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="d606d-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="d606d-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="d606d-120">Se elimina la transferencia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d606d-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="d606d-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="d606d-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="d606d-122">La transferencia del mensaje está en curso.</span><span class="sxs-lookup"><span data-stu-id="d606d-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d606d-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d606d-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d606d-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d606d-124">Header files</span></span>

<span data-ttu-id="d606d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d606d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d606d-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d606d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d606d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d606d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d606d-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d606d-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d606d-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d606d-129">See also</span></span>



[<span data-ttu-id="d606d-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d606d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d606d-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d606d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d606d-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d606d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d606d-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d606d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

