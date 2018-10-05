---
title: Propiedad canónica PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400337"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="4a9b9-103">Propiedad canónica PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="4a9b9-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="4a9b9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a9b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a9b9-105">El nombre del componente de dirección URL para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a9b9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4a9b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a9b9-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4a9b9-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4a9b9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a9b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a9b9-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="4a9b9-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="4a9b9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4a9b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a9b9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a9b9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a9b9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a9b9-112">Area:</span></span>  <br/> |<span data-ttu-id="4a9b9-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="4a9b9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a9b9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a9b9-114">Remarks</span></span>

<span data-ttu-id="4a9b9-115">Estas propiedades deben ser únicas dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="4a9b9-116">Si no se conjunto cuando se crea el mensaje, el almacén de mensajes debe establecer estas propiedades en función de diversas propiedades del mensaje, según la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="4a9b9-117">Por ejemplo, el **IPM. Nota** y **IPM. Cita** mensajes deben tienen esta propiedad establecida en función de la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y la **IPM. Contacto** mensajes deben tener esta propiedad establece en función de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4a9b9-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="4a9b9-118">Para la mayoría de clases de mensaje, esta propiedad debe basarse en la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4a9b9-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a9b9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a9b9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a9b9-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4a9b9-120">Protocol specifications</span></span>

<span data-ttu-id="4a9b9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a9b9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a9b9-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a9b9-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a9b9-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a9b9-124">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4a9b9-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a9b9-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a9b9-126">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a9b9-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4a9b9-127">Header files</span></span>

<span data-ttu-id="4a9b9-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a9b9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a9b9-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a9b9-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a9b9-130">Mapitags.h</span></span>
  
> <span data-ttu-id="4a9b9-131">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4a9b9-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a9b9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a9b9-132">See also</span></span>



[<span data-ttu-id="4a9b9-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a9b9-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a9b9-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4a9b9-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a9b9-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4a9b9-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a9b9-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4a9b9-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

