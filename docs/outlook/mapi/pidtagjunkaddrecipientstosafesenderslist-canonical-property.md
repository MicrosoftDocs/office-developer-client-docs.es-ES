---
title: Propiedad canónica PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282371"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="b35e5-103">Propiedad canónica PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="b35e5-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="b35e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b35e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b35e5-105">Indica si los destinatarios de correo se van a agregar a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="b35e5-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b35e5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b35e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b35e5-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="b35e5-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="b35e5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b35e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b35e5-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="b35e5-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="b35e5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b35e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="b35e5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b35e5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b35e5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b35e5-112">Area:</span></span>  <br/> |<span data-ttu-id="b35e5-113">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="b35e5-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b35e5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b35e5-114">Remarks</span></span>

<span data-ttu-id="b35e5-115">Si está presente, esta propiedad debe establecerse en 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="b35e5-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="b35e5-116">Un valor de 1 indica que los destinatarios de correo se deben agregar a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="b35e5-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="b35e5-117">Un valor de 0 indica que los destinatarios de correo no se deben agregar a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="b35e5-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="b35e5-118">Si esta propiedad está presente con un valor de 1, las direcciones SMTP de los destinatarios de correo electrónico deben agregarse a la cláusula de remitentes de confianza de la condición regla de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="b35e5-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="b35e5-119">Si esta propiedad es 0, no se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="b35e5-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b35e5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b35e5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b35e5-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b35e5-121">Protocol specifications</span></span>

<span data-ttu-id="b35e5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b35e5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b35e5-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b35e5-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b35e5-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b35e5-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b35e5-125">Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="b35e5-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b35e5-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b35e5-126">Header files</span></span>

<span data-ttu-id="b35e5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b35e5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b35e5-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b35e5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b35e5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b35e5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b35e5-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b35e5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b35e5-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b35e5-131">See also</span></span>



[<span data-ttu-id="b35e5-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b35e5-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b35e5-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b35e5-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b35e5-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b35e5-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b35e5-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b35e5-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

