---
title: Propiedad canónico PidTagProviderSubmitTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 162451d000c0b3da42c8fbef5f64459bc5ae23b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819977"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="22630-103">Propiedad canónico PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="22630-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="22630-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22630-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22630-105">Contiene la fecha y hora que había pasado de un proveedor de transporte de un mensaje a su sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="22630-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22630-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="22630-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22630-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="22630-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="22630-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="22630-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22630-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="22630-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="22630-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="22630-110">Data type:</span></span>  <br/> |<span data-ttu-id="22630-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="22630-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="22630-112">Área:</span><span class="sxs-lookup"><span data-stu-id="22630-112">Area:</span></span>  <br/> |<span data-ttu-id="22630-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="22630-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22630-114">Notas</span><span class="sxs-lookup"><span data-stu-id="22630-114">Remarks</span></span>

<span data-ttu-id="22630-115">Esta propiedad se establece por el proveedor de transporte saliente en el momento en que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="22630-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="22630-116">Esta propiedad corresponde a un atributo de cada mensaje X.400 envelope de envío.</span><span class="sxs-lookup"><span data-stu-id="22630-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="22630-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="22630-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="22630-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="22630-118">Header files</span></span>

<span data-ttu-id="22630-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22630-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="22630-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="22630-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="22630-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22630-121">Mapitags.h</span></span>
  
> <span data-ttu-id="22630-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="22630-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22630-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="22630-123">See also</span></span>



[<span data-ttu-id="22630-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="22630-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22630-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="22630-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22630-126">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="22630-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22630-127">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="22630-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

