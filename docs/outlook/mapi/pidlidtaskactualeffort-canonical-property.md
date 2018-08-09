---
title: Propiedad canónica PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818933"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="c57be-103">Propiedad canónica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="c57be-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="c57be-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c57be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c57be-105">Indica el número de minutos que el usuario ha realizado una tarea.</span><span class="sxs-lookup"><span data-stu-id="c57be-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c57be-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c57be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c57be-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="c57be-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="c57be-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c57be-108">Property set:</span></span>  <br/> |<span data-ttu-id="c57be-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c57be-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c57be-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="c57be-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c57be-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="c57be-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="c57be-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c57be-112">Data type:</span></span>  <br/> |<span data-ttu-id="c57be-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c57be-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c57be-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c57be-114">Area:</span></span>  <br/> |<span data-ttu-id="c57be-115">Task</span><span class="sxs-lookup"><span data-stu-id="c57be-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c57be-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c57be-116">Remarks</span></span>

<span data-ttu-id="c57be-117">El valor debe ser mayor o igual a 0 y menor que 0x5AE980DF (1,525,252,319), donde 480 minutos igual a un día y 2400 minutos igual una semana (ocho horas en un día de trabajo y cinco días en una semana de trabajo).</span><span class="sxs-lookup"><span data-stu-id="c57be-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c57be-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c57be-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c57be-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c57be-119">Protocol specifications</span></span>

<span data-ttu-id="c57be-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57be-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57be-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c57be-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c57be-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57be-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57be-123">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="c57be-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c57be-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c57be-124">Header files</span></span>

<span data-ttu-id="c57be-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c57be-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c57be-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c57be-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c57be-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c57be-127">See also</span></span>



[<span data-ttu-id="c57be-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c57be-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c57be-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c57be-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c57be-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c57be-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c57be-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c57be-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

