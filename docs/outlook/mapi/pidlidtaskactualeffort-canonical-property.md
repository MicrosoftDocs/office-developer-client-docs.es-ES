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
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331174"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="f9f35-103">Propiedad canónica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="f9f35-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="f9f35-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9f35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9f35-105">Indica el número de minutos que el usuario realizó una tarea.</span><span class="sxs-lookup"><span data-stu-id="f9f35-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9f35-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f9f35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9f35-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="f9f35-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="f9f35-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f9f35-108">Property set:</span></span>  <br/> |<span data-ttu-id="f9f35-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f9f35-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f9f35-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f9f35-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f9f35-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="f9f35-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="f9f35-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f9f35-112">Data type:</span></span>  <br/> |<span data-ttu-id="f9f35-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f9f35-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f9f35-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f9f35-114">Area:</span></span>  <br/> |<span data-ttu-id="f9f35-115">Task</span><span class="sxs-lookup"><span data-stu-id="f9f35-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9f35-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9f35-116">Remarks</span></span>

<span data-ttu-id="f9f35-117">El valor debe ser mayor o igual que 0 y menor que 0x5AE980DF (1.525.252.319), donde 480 minutos equivalen a un día y 2400 minutos a una semana (ocho horas en un día laborable y cinco días en una semana laboral).</span><span class="sxs-lookup"><span data-stu-id="f9f35-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9f35-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9f35-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9f35-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f9f35-119">Protocol specifications</span></span>

<span data-ttu-id="f9f35-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9f35-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9f35-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f9f35-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9f35-122">[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9f35-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9f35-123">Especifica las propiedades y operaciones permitidas para los objetos de lista de distribución personal y de contacto.</span><span class="sxs-lookup"><span data-stu-id="f9f35-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9f35-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f9f35-124">Header files</span></span>

<span data-ttu-id="f9f35-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9f35-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9f35-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f9f35-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9f35-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9f35-127">See also</span></span>



[<span data-ttu-id="f9f35-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f9f35-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9f35-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f9f35-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9f35-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f9f35-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9f35-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f9f35-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

