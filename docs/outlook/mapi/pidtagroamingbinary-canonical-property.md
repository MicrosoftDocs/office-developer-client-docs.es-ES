---
title: Propiedad canónica PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401674"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="f127e-103">Propiedad canónica PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="f127e-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="f127e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f127e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f127e-105">Contiene una secuencia de mensaje asociada a una subclase de la **IPM. Configuración** clase.</span><span class="sxs-lookup"><span data-stu-id="f127e-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f127e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f127e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f127e-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="f127e-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="f127e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f127e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f127e-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="f127e-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="f127e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f127e-110">Data type:</span></span>  <br/> |<span data-ttu-id="f127e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f127e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f127e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f127e-112">Area:</span></span>  <br/> |<span data-ttu-id="f127e-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="f127e-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f127e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f127e-114">Remarks</span></span>

<span data-ttu-id="f127e-115">Esta propiedad contiene la secuencia de datos asociada a un **IPM. Configuración** mensaje de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f127e-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="f127e-116">El formato de la secuencia depende de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f127e-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="f127e-117">Por ejemplo, un mensaje de tipo de clase **IPM. Configuration.Autocomplete** adoptarán el formato como una [secuencia de Autocompletar](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="f127e-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f127e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f127e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f127e-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f127e-119">Protocol specifications</span></span>

<span data-ttu-id="f127e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f127e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f127e-121">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f127e-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f127e-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f127e-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f127e-123">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f127e-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f127e-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f127e-124">Header files</span></span>

<span data-ttu-id="f127e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f127e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f127e-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f127e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f127e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f127e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f127e-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f127e-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f127e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f127e-129">See also</span></span>



[<span data-ttu-id="f127e-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f127e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f127e-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f127e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f127e-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f127e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f127e-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f127e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

