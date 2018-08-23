---
title: Propiedad canónica PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588275"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="a55f6-103">Propiedad canónica PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="a55f6-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="a55f6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a55f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a55f6-105">Indica un tiempo cuando un cliente que le gustaría aplazar el envío de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a55f6-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a55f6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a55f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a55f6-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="a55f6-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="a55f6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a55f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a55f6-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="a55f6-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="a55f6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a55f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="a55f6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a55f6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a55f6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a55f6-112">Area:</span></span>  <br/> |<span data-ttu-id="a55f6-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="a55f6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a55f6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a55f6-114">Remarks</span></span>

<span data-ttu-id="a55f6-115">Si las propiedades de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) y **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) están presentes, se vuelve a calcular el valor de esta propiedad mediante el uso de la siguiente fórmula y se omite el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="a55f6-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="a55f6-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="a55f6-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="a55f6-117">Si el valor **PR_DEFERRED_SEND_TIME** es anterior a la hora actual (en UTC), el mensaje se envía inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a55f6-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a55f6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a55f6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a55f6-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a55f6-119">Protocol specifications</span></span>

<span data-ttu-id="a55f6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a55f6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a55f6-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a55f6-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a55f6-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a55f6-122">Header files</span></span>

<span data-ttu-id="a55f6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a55f6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a55f6-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a55f6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a55f6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a55f6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a55f6-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a55f6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a55f6-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a55f6-127">See also</span></span>



[<span data-ttu-id="a55f6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a55f6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a55f6-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a55f6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a55f6-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a55f6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a55f6-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a55f6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

