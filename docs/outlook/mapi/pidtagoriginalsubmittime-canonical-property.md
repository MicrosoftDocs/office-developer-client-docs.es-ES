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
ms.openlocfilehash: 31324dff3c5780f693b1dc055fc2067436496cd3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573652"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="630c8-103">Propiedad canónica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="630c8-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="630c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="630c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="630c8-105">Contiene la fecha de envío original y la hora del mensaje en el informe.</span><span class="sxs-lookup"><span data-stu-id="630c8-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="630c8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="630c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="630c8-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="630c8-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="630c8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="630c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="630c8-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="630c8-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="630c8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="630c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="630c8-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="630c8-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="630c8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="630c8-112">Area:</span></span>  <br/> |<span data-ttu-id="630c8-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="630c8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="630c8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="630c8-114">Remarks</span></span>

<span data-ttu-id="630c8-115">En el primer envío de un mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="630c8-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="630c8-116">No se cambia cuando se reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="630c8-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="630c8-117">Esta opción se usa sólo informes.</span><span class="sxs-lookup"><span data-stu-id="630c8-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="630c8-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="630c8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="630c8-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="630c8-119">Protocol specifications</span></span>

<span data-ttu-id="630c8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630c8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630c8-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="630c8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="630c8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630c8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630c8-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="630c8-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="630c8-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="630c8-124">Header files</span></span>

<span data-ttu-id="630c8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="630c8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="630c8-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="630c8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="630c8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="630c8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="630c8-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="630c8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="630c8-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="630c8-129">See also</span></span>



[<span data-ttu-id="630c8-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="630c8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="630c8-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="630c8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="630c8-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="630c8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="630c8-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="630c8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

