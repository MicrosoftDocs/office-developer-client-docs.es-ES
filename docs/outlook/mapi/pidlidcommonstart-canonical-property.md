---
title: Propiedad canónica PidLidCommonStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e2d3dee4d268a1747d6b77acf62f24c6ec459bdc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818600"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="96e53-103">Propiedad canónica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="96e53-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="96e53-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96e53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96e53-105">Representa la fecha de inicio y la hora de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96e53-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96e53-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="96e53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96e53-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="96e53-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="96e53-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="96e53-108">Property set:</span></span>  <br/> |<span data-ttu-id="96e53-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="96e53-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="96e53-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="96e53-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="96e53-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="96e53-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="96e53-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="96e53-112">Data type:</span></span>  <br/> |<span data-ttu-id="96e53-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="96e53-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="96e53-114">Área:</span><span class="sxs-lookup"><span data-stu-id="96e53-114">Area:</span></span>  <br/> |<span data-ttu-id="96e53-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="96e53-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96e53-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96e53-116">Remarks</span></span>

<span data-ttu-id="96e53-117">Esta propiedad indica la hora de inicio de un elemento.</span><span class="sxs-lookup"><span data-stu-id="96e53-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="96e53-118">Debe ser menor o igual que el valor de la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96e53-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="96e53-119">El valor de esta propiedad debe ser el equivalente de hora Universal coordinada (UTC) de la propiedad **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96e53-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96e53-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96e53-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96e53-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="96e53-121">Protocol specifications</span></span>

<span data-ttu-id="96e53-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96e53-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96e53-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="96e53-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96e53-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96e53-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96e53-125">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e53-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="96e53-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96e53-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96e53-127">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="96e53-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96e53-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="96e53-128">Header files</span></span>

<span data-ttu-id="96e53-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96e53-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="96e53-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="96e53-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96e53-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="96e53-131">See also</span></span>



[<span data-ttu-id="96e53-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96e53-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96e53-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="96e53-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96e53-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="96e53-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96e53-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="96e53-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

