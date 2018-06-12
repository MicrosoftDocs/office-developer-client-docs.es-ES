---
title: Propiedad canónico PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818789"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="00627-103">Propiedad canónico PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="00627-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="00627-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00627-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00627-105">Representa la fecha de finalización y la hora para el mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="00627-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00627-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="00627-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00627-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="00627-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="00627-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="00627-108">Property set:</span></span>  <br/> |<span data-ttu-id="00627-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="00627-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="00627-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="00627-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00627-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="00627-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="00627-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="00627-112">Data type:</span></span>  <br/> |<span data-ttu-id="00627-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="00627-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="00627-114">Área:</span><span class="sxs-lookup"><span data-stu-id="00627-114">Area:</span></span>  <br/> |<span data-ttu-id="00627-115">Journal</span><span class="sxs-lookup"><span data-stu-id="00627-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00627-116">Notas</span><span class="sxs-lookup"><span data-stu-id="00627-116">Remarks</span></span>

<span data-ttu-id="00627-117">La hora en que la actividad finalizó en hora Universal coordinada el (UTC), que debe ser igual a la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) y mayor o igual que la propiedad **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="00627-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00627-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00627-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00627-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="00627-119">Protocol specifications</span></span>

<span data-ttu-id="00627-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00627-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00627-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="00627-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00627-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00627-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00627-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="00627-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00627-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="00627-124">Header files</span></span>

<span data-ttu-id="00627-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00627-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="00627-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="00627-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00627-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="00627-127">See also</span></span>



[<span data-ttu-id="00627-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00627-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00627-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="00627-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00627-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="00627-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00627-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="00627-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

