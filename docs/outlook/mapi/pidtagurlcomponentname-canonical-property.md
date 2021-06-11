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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320429"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="18872-103">Propiedad canónica PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="18872-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="18872-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18872-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18872-105">El nombre del componente de dirección URL de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="18872-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18872-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="18872-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18872-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="18872-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="18872-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="18872-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18872-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="18872-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="18872-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="18872-110">Data type:</span></span>  <br/> |<span data-ttu-id="18872-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18872-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="18872-112">Área:</span><span class="sxs-lookup"><span data-stu-id="18872-112">Area:</span></span>  <br/> |<span data-ttu-id="18872-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="18872-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18872-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18872-114">Remarks</span></span>

<span data-ttu-id="18872-115">Estas propiedades deben ser únicas dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="18872-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="18872-116">Si no se establece cuando se crea el mensaje, el almacén de mensajes debe establecer estas propiedades en función de varias propiedades de mensaje, según la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="18872-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="18872-117">Por ejemplo, **el IPM. Nota** e **IPM. Los** mensajes de cita deben tener esta propiedad establecida en función **de la propiedad PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y el **IPM. Los** mensajes de contacto deben tener esta propiedad establecida en función de la **propiedad dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18872-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="18872-118">Para la mayoría de las demás clases de mensaje, esta propiedad debe basarse en la **propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18872-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18872-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="18872-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18872-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="18872-120">Protocol specifications</span></span>

<span data-ttu-id="18872-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18872-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18872-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="18872-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18872-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18872-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18872-124">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="18872-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="18872-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18872-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18872-126">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="18872-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18872-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="18872-127">Header files</span></span>

<span data-ttu-id="18872-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18872-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="18872-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="18872-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="18872-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18872-130">Mapitags.h</span></span>
  
> <span data-ttu-id="18872-131">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="18872-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18872-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="18872-132">See also</span></span>



[<span data-ttu-id="18872-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="18872-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18872-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="18872-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18872-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="18872-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18872-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="18872-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

