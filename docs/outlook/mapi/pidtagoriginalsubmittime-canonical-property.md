---
title: Propiedad canónica PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 43d0387f1c25c5ac86168caaddddd9fb9171c827
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819854"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="e544f-103">Propiedad canónica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="e544f-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="e544f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e544f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e544f-105">Contiene la fecha de envío original y la hora del mensaje en el informe.</span><span class="sxs-lookup"><span data-stu-id="e544f-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e544f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e544f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e544f-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="e544f-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="e544f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e544f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e544f-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="e544f-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="e544f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e544f-110">Data type:</span></span>  <br/> |<span data-ttu-id="e544f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e544f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e544f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e544f-112">Area:</span></span>  <br/> |<span data-ttu-id="e544f-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="e544f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e544f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e544f-114">Remarks</span></span>

<span data-ttu-id="e544f-115">En el primer envío de un mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e544f-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="e544f-116">No se cambia cuando se reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e544f-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="e544f-117">Esta opción se usa sólo informes.</span><span class="sxs-lookup"><span data-stu-id="e544f-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e544f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e544f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e544f-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e544f-119">Protocol specifications</span></span>

<span data-ttu-id="e544f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e544f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e544f-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e544f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e544f-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e544f-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e544f-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e544f-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e544f-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e544f-124">Header files</span></span>

<span data-ttu-id="e544f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e544f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e544f-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e544f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e544f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e544f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e544f-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e544f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e544f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e544f-129">See also</span></span>



[<span data-ttu-id="e544f-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e544f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e544f-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e544f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e544f-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e544f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e544f-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e544f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

