---
title: Propiedad canónico PidLidTaskActualEffort
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818933"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="25755-103">Propiedad canónico PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="25755-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="25755-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25755-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25755-105">Indica el número de minutos que el usuario ha realizado una tarea.</span><span class="sxs-lookup"><span data-stu-id="25755-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25755-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="25755-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25755-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="25755-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="25755-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="25755-108">Property set:</span></span>  <br/> |<span data-ttu-id="25755-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="25755-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="25755-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="25755-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25755-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="25755-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="25755-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="25755-112">Data type:</span></span>  <br/> |<span data-ttu-id="25755-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25755-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25755-114">Área:</span><span class="sxs-lookup"><span data-stu-id="25755-114">Area:</span></span>  <br/> |<span data-ttu-id="25755-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="25755-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25755-116">Notas</span><span class="sxs-lookup"><span data-stu-id="25755-116">Remarks</span></span>

<span data-ttu-id="25755-117">El valor debe ser mayor o igual a 0 y menor que 0x5AE980DF (1,525,252,319), donde 480 minutos igual a un día y 2400 minutos igual una semana (ocho horas en un día de trabajo y cinco días en una semana de trabajo).</span><span class="sxs-lookup"><span data-stu-id="25755-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25755-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="25755-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25755-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="25755-119">Protocol specifications</span></span>

<span data-ttu-id="25755-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25755-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25755-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="25755-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25755-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25755-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25755-123">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="25755-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25755-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="25755-124">Header files</span></span>

<span data-ttu-id="25755-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25755-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="25755-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="25755-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25755-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="25755-127">See also</span></span>



[<span data-ttu-id="25755-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="25755-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25755-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="25755-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25755-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="25755-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25755-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="25755-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

