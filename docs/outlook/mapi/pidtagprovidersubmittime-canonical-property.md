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
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="2e25b-103">Propiedad canónica PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="2e25b-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="2e25b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e25b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e25b-105">Contiene la fecha y la hora en que un proveedor de transporte pasó un mensaje a su sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="2e25b-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e25b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2e25b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e25b-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="2e25b-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="2e25b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2e25b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e25b-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="2e25b-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="2e25b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2e25b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e25b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2e25b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2e25b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2e25b-112">Area:</span></span>  <br/> |<span data-ttu-id="2e25b-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="2e25b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e25b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e25b-114">Remarks</span></span>

<span data-ttu-id="2e25b-115">El proveedor de transporte saliente establece esta propiedad en el momento en que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="2e25b-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="2e25b-116">Esta propiedad corresponde a un atributo de sobre de envío X.400 por mensaje.</span><span class="sxs-lookup"><span data-stu-id="2e25b-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e25b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e25b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e25b-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2e25b-118">Header files</span></span>

<span data-ttu-id="2e25b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e25b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e25b-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2e25b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e25b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e25b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2e25b-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2e25b-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e25b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2e25b-123">See also</span></span>



[<span data-ttu-id="2e25b-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2e25b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e25b-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2e25b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e25b-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2e25b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e25b-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2e25b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

