---
title: Propiedad canónico PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cc2d52ec183cc336bf126b1fda9a85d41f704f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818791"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="e3f90-103">Propiedad canónico PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="e3f90-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="e3f90-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3f90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3f90-105">Representa la duración, en minutos, de un mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="e3f90-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3f90-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e3f90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3f90-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="e3f90-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="e3f90-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e3f90-108">Property set:</span></span>  <br/> |<span data-ttu-id="e3f90-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="e3f90-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="e3f90-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e3f90-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e3f90-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="e3f90-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="e3f90-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e3f90-112">Data type:</span></span>  <br/> |<span data-ttu-id="e3f90-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e3f90-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e3f90-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e3f90-114">Area:</span></span>  <br/> |<span data-ttu-id="e3f90-115">Journal</span><span class="sxs-lookup"><span data-stu-id="e3f90-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3f90-116">Notas</span><span class="sxs-lookup"><span data-stu-id="e3f90-116">Remarks</span></span>

<span data-ttu-id="e3f90-117">La duración, en minutos, de la actividad que debe ser la diferencia entre las propiedades de **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) y **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e3f90-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e3f90-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3f90-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3f90-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e3f90-119">Protocol specifications</span></span>

<span data-ttu-id="e3f90-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3f90-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3f90-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e3f90-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3f90-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3f90-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3f90-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="e3f90-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3f90-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e3f90-124">Header files</span></span>

<span data-ttu-id="e3f90-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3f90-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3f90-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e3f90-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3f90-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="e3f90-127">See also</span></span>



[<span data-ttu-id="e3f90-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3f90-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3f90-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e3f90-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3f90-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="e3f90-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3f90-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e3f90-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

