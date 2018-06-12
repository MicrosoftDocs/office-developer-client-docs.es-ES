---
title: Propiedad canónico PidTagJunkAddRecipientsToSafeSendersList
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819661"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="87f02-103">Propiedad canónico PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="87f02-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="87f02-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87f02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87f02-105">Indica si están o no los destinatarios de correo que se agregará a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="87f02-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87f02-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="87f02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87f02-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="87f02-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="87f02-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="87f02-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87f02-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="87f02-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="87f02-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="87f02-110">Data type:</span></span>  <br/> |<span data-ttu-id="87f02-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87f02-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87f02-112">Área:</span><span class="sxs-lookup"><span data-stu-id="87f02-112">Area:</span></span>  <br/> |<span data-ttu-id="87f02-113">Spam</span><span class="sxs-lookup"><span data-stu-id="87f02-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87f02-114">Notas</span><span class="sxs-lookup"><span data-stu-id="87f02-114">Remarks</span></span>

<span data-ttu-id="87f02-115">Si está presente, esta propiedad debe establecerse en 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="87f02-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="87f02-116">Un valor de 1 indica que los destinatarios de correo deben agregarse a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="87f02-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="87f02-117">Un valor de 0 indica que los destinatarios de correo no se agregará a la lista de remitentes seguros.</span><span class="sxs-lookup"><span data-stu-id="87f02-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="87f02-118">Si esta propiedad está presente con un valor de 1, las direcciones SMTP de los destinatarios de correo electrónico deben agregarse a la cláusula de remitentes de confianza de la condición de regla de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="87f02-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="87f02-119">Si esta propiedad es 0, se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="87f02-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87f02-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="87f02-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87f02-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="87f02-121">Protocol specifications</span></span>

<span data-ttu-id="87f02-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87f02-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87f02-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="87f02-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87f02-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87f02-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87f02-125">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="87f02-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87f02-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="87f02-126">Header files</span></span>

<span data-ttu-id="87f02-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87f02-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="87f02-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="87f02-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="87f02-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87f02-129">Mapitags.h</span></span>
  
> <span data-ttu-id="87f02-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="87f02-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87f02-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="87f02-131">See also</span></span>



[<span data-ttu-id="87f02-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="87f02-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87f02-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="87f02-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87f02-134">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="87f02-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87f02-135">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="87f02-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

