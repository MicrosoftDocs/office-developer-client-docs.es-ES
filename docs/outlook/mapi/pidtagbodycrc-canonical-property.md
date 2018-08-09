---
title: Propiedad canónica PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819283"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="8ed0d-103">Propiedad canónica PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="8ed0d-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="8ed0d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ed0d-105">Contiene un valor de redundancia cíclica (CRC) de verificación en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed0d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ed0d-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="8ed0d-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="8ed0d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ed0d-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="8ed0d-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="8ed0d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ed0d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8ed0d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8ed0d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-112">Area:</span></span>  <br/> |<span data-ttu-id="8ed0d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8ed0d-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed0d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ed0d-114">Remarks</span></span>

<span data-ttu-id="8ed0d-115">El almacén de mensajes puede utilizar cualquier algoritmo CRC que genera un valor PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="8ed0d-116">Debe calcular esta propiedad como parte del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) cuando se ha establecido la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) por primera vez y siempre que se ha modificado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="8ed0d-117">Una aplicación cliente usa **PR_BODY_CRC** para facilitar la comparación de las cadenas de texto de mensaje contenidas en las propiedades **PR_BODY** o sus variantes.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="8ed0d-118">Uso de esta propiedad, el cliente puede rápida y fácilmente detectar cuándo ha cambiado el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="8ed0d-119">Pueden obtener mejoras significativas del rendimiento mediante el uso de **PR_BODY_CRC** en lugar de obtener **PR_BODY** desde el almacén de mensajes y la compara con una versión local.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ed0d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed0d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ed0d-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8ed0d-121">Header files</span></span>

<span data-ttu-id="8ed0d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ed0d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ed0d-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ed0d-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ed0d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8ed0d-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed0d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed0d-126">See also</span></span>



[<span data-ttu-id="8ed0d-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed0d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ed0d-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8ed0d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ed0d-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed0d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ed0d-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8ed0d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

