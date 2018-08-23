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
ms.openlocfilehash: 55da942e59c619dd384bef58349aa3a00d4a6d8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571475"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="71c14-103">Propiedad canónica PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="71c14-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="71c14-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71c14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71c14-105">Contiene un valor de redundancia cíclica (CRC) de verificación en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="71c14-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71c14-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="71c14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71c14-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="71c14-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="71c14-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="71c14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71c14-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="71c14-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="71c14-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="71c14-110">Data type:</span></span>  <br/> |<span data-ttu-id="71c14-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="71c14-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="71c14-112">Área:</span><span class="sxs-lookup"><span data-stu-id="71c14-112">Area:</span></span>  <br/> |<span data-ttu-id="71c14-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="71c14-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71c14-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71c14-114">Remarks</span></span>

<span data-ttu-id="71c14-115">El almacén de mensajes puede utilizar cualquier algoritmo CRC que genera un valor PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="71c14-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="71c14-116">Debe calcular esta propiedad como parte del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) cuando se ha establecido la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) por primera vez y siempre que se ha modificado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="71c14-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="71c14-117">Una aplicación cliente usa **PR_BODY_CRC** para facilitar la comparación de las cadenas de texto de mensaje contenidas en las propiedades **PR_BODY** o sus variantes.</span><span class="sxs-lookup"><span data-stu-id="71c14-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="71c14-118">Uso de esta propiedad, el cliente puede rápida y fácilmente detectar cuándo ha cambiado el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="71c14-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="71c14-119">Pueden obtener mejoras significativas del rendimiento mediante el uso de **PR_BODY_CRC** en lugar de obtener **PR_BODY** desde el almacén de mensajes y la compara con una versión local.</span><span class="sxs-lookup"><span data-stu-id="71c14-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="71c14-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="71c14-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="71c14-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="71c14-121">Header files</span></span>

<span data-ttu-id="71c14-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71c14-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="71c14-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="71c14-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="71c14-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71c14-124">Mapitags.h</span></span>
  
> <span data-ttu-id="71c14-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="71c14-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71c14-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="71c14-126">See also</span></span>



[<span data-ttu-id="71c14-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="71c14-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71c14-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="71c14-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71c14-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="71c14-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71c14-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="71c14-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

