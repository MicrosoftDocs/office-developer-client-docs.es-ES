---
title: Propiedad canónico PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a31e2862aa3a6265f1dd9f8036abe329cf556276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818999"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="22845-103">Propiedad canónico PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="22845-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="22845-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22845-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22845-105">Indica qué copia es la actualización más reciente de una tarea.</span><span class="sxs-lookup"><span data-stu-id="22845-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22845-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="22845-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22845-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="22845-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="22845-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="22845-108">Property set:</span></span>  <br/> |<span data-ttu-id="22845-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="22845-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="22845-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="22845-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22845-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="22845-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="22845-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="22845-112">Data type:</span></span>  <br/> |<span data-ttu-id="22845-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22845-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22845-114">Área:</span><span class="sxs-lookup"><span data-stu-id="22845-114">Area:</span></span>  <br/> |<span data-ttu-id="22845-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="22845-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22845-116">Notas</span><span class="sxs-lookup"><span data-stu-id="22845-116">Remarks</span></span>

<span data-ttu-id="22845-117">Se omiten las actualizaciones con versiones inferiores a la tarea.</span><span class="sxs-lookup"><span data-stu-id="22845-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="22845-118">Incrustación de una tarea en una comunicación de la tarea, el cliente establece la versión actual de la tarea incrustada en así como la comunicación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="22845-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22845-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="22845-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22845-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="22845-120">Protocol specifications</span></span>

<span data-ttu-id="22845-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22845-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22845-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="22845-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22845-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22845-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22845-124">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="22845-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22845-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="22845-125">Header files</span></span>

<span data-ttu-id="22845-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22845-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="22845-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="22845-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22845-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="22845-128">See also</span></span>



[<span data-ttu-id="22845-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="22845-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22845-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="22845-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22845-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="22845-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22845-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="22845-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

