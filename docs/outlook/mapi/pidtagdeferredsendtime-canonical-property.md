---
title: Propiedad canónico PidTagDeferredSendTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3912c429f1aa932b4956d943579a4ed99634dca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819411"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="15429-103">Propiedad canónico PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="15429-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="15429-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15429-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15429-105">Indica un tiempo cuando un cliente que le gustaría aplazar el envío de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="15429-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15429-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="15429-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15429-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="15429-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="15429-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="15429-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15429-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="15429-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="15429-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="15429-110">Data type:</span></span>  <br/> |<span data-ttu-id="15429-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="15429-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="15429-112">Área:</span><span class="sxs-lookup"><span data-stu-id="15429-112">Area:</span></span>  <br/> |<span data-ttu-id="15429-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="15429-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15429-114">Notas</span><span class="sxs-lookup"><span data-stu-id="15429-114">Remarks</span></span>

<span data-ttu-id="15429-115">Si las propiedades de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) y **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) están presentes, se vuelve a calcular el valor de esta propiedad mediante el uso de la siguiente fórmula y se omite el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="15429-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="15429-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="15429-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="15429-117">Si el valor **PR_DEFERRED_SEND_TIME** es anterior a la hora actual (en UTC), el mensaje se envía inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="15429-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="15429-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="15429-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15429-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="15429-119">Protocol specifications</span></span>

<span data-ttu-id="15429-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15429-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15429-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="15429-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15429-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="15429-122">Header files</span></span>

<span data-ttu-id="15429-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15429-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="15429-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="15429-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="15429-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15429-125">Mapitags.h</span></span>
  
> <span data-ttu-id="15429-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="15429-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15429-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="15429-127">See also</span></span>



[<span data-ttu-id="15429-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="15429-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15429-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="15429-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15429-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="15429-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15429-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="15429-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

