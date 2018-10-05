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
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385735"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="5f6b1-103">Propiedad canónica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="5f6b1-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="5f6b1-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f6b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f6b1-105">Contiene la fecha de envío original y la hora del mensaje en el informe.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f6b1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5f6b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f6b1-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="5f6b1-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="5f6b1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5f6b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f6b1-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="5f6b1-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="5f6b1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5f6b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f6b1-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f6b1-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5f6b1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5f6b1-112">Area:</span></span>  <br/> |<span data-ttu-id="5f6b1-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="5f6b1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f6b1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f6b1-114">Remarks</span></span>

<span data-ttu-id="5f6b1-115">En el primer envío de un mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f6b1-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="5f6b1-116">No se cambia cuando se reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="5f6b1-117">Esta opción se usa sólo informes.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f6b1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f6b1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f6b1-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f6b1-119">Protocol specifications</span></span>

<span data-ttu-id="5f6b1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f6b1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f6b1-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f6b1-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f6b1-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f6b1-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f6b1-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5f6b1-124">Header files</span></span>

<span data-ttu-id="5f6b1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f6b1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f6b1-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f6b1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f6b1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5f6b1-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5f6b1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f6b1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f6b1-129">See also</span></span>



[<span data-ttu-id="5f6b1-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f6b1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f6b1-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5f6b1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f6b1-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5f6b1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f6b1-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5f6b1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

