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
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="85463-103">Propiedad canónica PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="85463-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="85463-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85463-105">Indica si los destinatarios de correo se van a agregar a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="85463-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85463-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="85463-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85463-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="85463-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="85463-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="85463-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85463-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="85463-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="85463-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="85463-110">Data type:</span></span>  <br/> |<span data-ttu-id="85463-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="85463-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="85463-112">Área:</span><span class="sxs-lookup"><span data-stu-id="85463-112">Area:</span></span>  <br/> |<span data-ttu-id="85463-113">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="85463-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85463-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85463-114">Remarks</span></span>

<span data-ttu-id="85463-115">Si está presente, esta propiedad debe establecerse en 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="85463-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="85463-116">Un valor de 1 indica que los destinatarios de correo se agregarán a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="85463-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="85463-117">Un valor de 0 indica que los destinatarios de correo no se van a agregar a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="85463-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="85463-118">Si esta propiedad está presente con un valor de 1, las direcciones SMTP de los destinatarios de correo electrónico deben agregarse a la cláusula de remitentes de confianza de la condición de regla de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="85463-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="85463-119">Si esta propiedad es 0, no se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="85463-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="85463-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="85463-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85463-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="85463-121">Protocol specifications</span></span>

<span data-ttu-id="85463-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85463-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85463-123">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="85463-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85463-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85463-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85463-125">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="85463-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85463-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="85463-126">Header files</span></span>

<span data-ttu-id="85463-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="85463-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="85463-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="85463-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="85463-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="85463-129">Mapitags.h</span></span>
  
> <span data-ttu-id="85463-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="85463-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85463-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="85463-131">See also</span></span>



[<span data-ttu-id="85463-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="85463-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85463-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="85463-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85463-134">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="85463-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85463-135">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="85463-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

