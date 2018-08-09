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
ms.openlocfilehash: 4fd74e99a8073db03ad47292677ff98efca58af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819729"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="c3719-103">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c3719-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c3719-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3719-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3719-105">Contiene la fecha y hora cuando un mensaje se entregó.</span><span class="sxs-lookup"><span data-stu-id="c3719-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3719-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c3719-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3719-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="c3719-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="c3719-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c3719-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3719-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="c3719-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="c3719-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c3719-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3719-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c3719-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c3719-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c3719-112">Area:</span></span>  <br/> |<span data-ttu-id="c3719-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="c3719-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3719-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3719-114">Remarks</span></span>

<span data-ttu-id="c3719-115">Esta propiedad describe el tiempo que el mensaje se almacena en el servidor, en lugar del tiempo de descarga cuando el proveedor de transporte copió el mensaje desde el servidor en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="c3719-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3719-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3719-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3719-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c3719-117">Protocol specifications</span></span>

<span data-ttu-id="c3719-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3719-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3719-119">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c3719-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3719-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c3719-120">Header files</span></span>

<span data-ttu-id="c3719-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3719-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3719-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c3719-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3719-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3719-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c3719-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c3719-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3719-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3719-125">See also</span></span>



[<span data-ttu-id="c3719-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c3719-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3719-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c3719-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3719-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c3719-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3719-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c3719-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

