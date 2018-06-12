---
title: Propiedad canónico PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 97650550704ba844f10131f1a3045ebbfaaaefff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820128"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="863dd-103">Propiedad canónico PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="863dd-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="863dd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="863dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="863dd-105">Contiene una secuencia de mensaje asociada a una subclase de la **IPM. Configuración** clase.</span><span class="sxs-lookup"><span data-stu-id="863dd-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="863dd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="863dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="863dd-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="863dd-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="863dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="863dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="863dd-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="863dd-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="863dd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="863dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="863dd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="863dd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="863dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="863dd-112">Area:</span></span>  <br/> |<span data-ttu-id="863dd-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="863dd-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="863dd-114">Notas</span><span class="sxs-lookup"><span data-stu-id="863dd-114">Remarks</span></span>

<span data-ttu-id="863dd-115">Esta propiedad contiene la secuencia de datos asociada a un **IPM. Configuración** mensaje de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="863dd-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="863dd-116">El formato de la secuencia depende de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="863dd-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="863dd-117">Por ejemplo, un mensaje de tipo de clase **IPM. Configuration.Autocomplete** adoptarán el formato como una [secuencia de Autocompletar](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="863dd-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="863dd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="863dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="863dd-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="863dd-119">Protocol specifications</span></span>

<span data-ttu-id="863dd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="863dd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="863dd-121">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="863dd-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="863dd-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="863dd-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="863dd-123">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="863dd-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="863dd-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="863dd-124">Header files</span></span>

<span data-ttu-id="863dd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="863dd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="863dd-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="863dd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="863dd-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="863dd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="863dd-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="863dd-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="863dd-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="863dd-129">See also</span></span>



[<span data-ttu-id="863dd-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="863dd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="863dd-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="863dd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="863dd-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="863dd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="863dd-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="863dd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

