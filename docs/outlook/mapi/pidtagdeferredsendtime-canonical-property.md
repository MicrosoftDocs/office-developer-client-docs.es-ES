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
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359881"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="b4e00-103">Propiedad canónica PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="b4e00-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="b4e00-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4e00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4e00-105">Indica una hora en la que un cliente desea aplazar el envío de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4e00-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4e00-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b4e00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4e00-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="b4e00-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="b4e00-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4e00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4e00-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="b4e00-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="b4e00-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b4e00-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4e00-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b4e00-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b4e00-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4e00-112">Area:</span></span>  <br/> |<span data-ttu-id="b4e00-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e00-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4e00-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4e00-114">Remarks</span></span>

<span data-ttu-id="b4e00-115">Si las **propiedades PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) y **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) están presentes, el valor de esta propiedad se vuelve a compilar mediante la fórmula siguiente y se omite el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="b4e00-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="b4e00-116">**PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="b4e00-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="b4e00-117">Si **PR_DEFERRED_SEND_TIME** valor es anterior a la hora actual (en UTC), el mensaje se envía inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b4e00-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b4e00-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4e00-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4e00-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b4e00-119">Protocol specifications</span></span>

<span data-ttu-id="b4e00-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4e00-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4e00-121">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b4e00-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4e00-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b4e00-122">Header files</span></span>

<span data-ttu-id="b4e00-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4e00-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4e00-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b4e00-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4e00-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4e00-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b4e00-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b4e00-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4e00-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b4e00-127">See also</span></span>



[<span data-ttu-id="b4e00-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e00-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4e00-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e00-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4e00-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e00-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4e00-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b4e00-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

