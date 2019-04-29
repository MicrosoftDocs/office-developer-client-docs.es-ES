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
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415183"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="da8a7-103">Propiedad canónica PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="da8a7-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="da8a7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da8a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da8a7-105">Contiene un valor de comprobación de redundancia cíclica (CRC) en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="da8a7-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da8a7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="da8a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da8a7-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="da8a7-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="da8a7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="da8a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da8a7-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="da8a7-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="da8a7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="da8a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="da8a7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da8a7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da8a7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="da8a7-112">Area:</span></span>  <br/> |<span data-ttu-id="da8a7-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="da8a7-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da8a7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da8a7-114">Remarks</span></span>

<span data-ttu-id="da8a7-115">El almacén de mensajes puede usar cualquier algoritmo CRC que genere un valor de PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="da8a7-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="da8a7-116">Debe calcular esta propiedad como parte del método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) cuando se ha establecido la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) por primera vez y siempre que se haya modificado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="da8a7-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="da8a7-117">Una aplicación cliente usa **PR_BODY_CRC** para facilitar la comparación de las cadenas de texto de mensaje contenidas en las propiedades de **PR_BODY** o sus variantes.</span><span class="sxs-lookup"><span data-stu-id="da8a7-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="da8a7-118">Mediante esta propiedad, el cliente puede detectar rápida y fácilmente cuándo cambia el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="da8a7-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="da8a7-119">Puede obtener ganancias de rendimiento considerables usando **PR_BODY_CRC** en lugar de obtener **PR_BODY** del almacén de mensajes y compararlo con una versión local.</span><span class="sxs-lookup"><span data-stu-id="da8a7-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="da8a7-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="da8a7-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="da8a7-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="da8a7-121">Header files</span></span>

<span data-ttu-id="da8a7-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="da8a7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="da8a7-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="da8a7-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="da8a7-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="da8a7-124">Mapitags.h</span></span>
  
> <span data-ttu-id="da8a7-125">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="da8a7-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da8a7-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="da8a7-126">See also</span></span>



[<span data-ttu-id="da8a7-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="da8a7-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da8a7-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="da8a7-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da8a7-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="da8a7-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da8a7-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="da8a7-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

