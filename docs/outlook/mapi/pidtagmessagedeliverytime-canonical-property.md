---
title: Propiedad canónica PidTagMessageDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325616"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="081ab-103">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="081ab-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="081ab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="081ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="081ab-105">Contiene la fecha y hora en que se entregó un mensaje.</span><span class="sxs-lookup"><span data-stu-id="081ab-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="081ab-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="081ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="081ab-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="081ab-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="081ab-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="081ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="081ab-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="081ab-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="081ab-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="081ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="081ab-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="081ab-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="081ab-112">Área:</span><span class="sxs-lookup"><span data-stu-id="081ab-112">Area:</span></span>  <br/> |<span data-ttu-id="081ab-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="081ab-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="081ab-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="081ab-114">Remarks</span></span>

<span data-ttu-id="081ab-115">Esta propiedad describe la hora en que se almacena el mensaje en el servidor, en lugar de la hora de descarga en la que el proveedor de transporte copió el mensaje del servidor al almacén local.</span><span class="sxs-lookup"><span data-stu-id="081ab-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="081ab-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="081ab-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="081ab-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="081ab-117">Protocol specifications</span></span>

<span data-ttu-id="081ab-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="081ab-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="081ab-119">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="081ab-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="081ab-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="081ab-120">Header files</span></span>

<span data-ttu-id="081ab-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="081ab-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="081ab-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="081ab-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="081ab-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="081ab-123">Mapitags.h</span></span>
  
> <span data-ttu-id="081ab-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="081ab-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="081ab-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="081ab-125">See also</span></span>



[<span data-ttu-id="081ab-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="081ab-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="081ab-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="081ab-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="081ab-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="081ab-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="081ab-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="081ab-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

