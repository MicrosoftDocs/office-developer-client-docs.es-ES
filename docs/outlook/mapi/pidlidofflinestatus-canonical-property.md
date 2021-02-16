---
title: Propiedad canónica PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418837"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="51c41-103">Propiedad canónica PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="51c41-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="51c41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c41-105">Determina el estado de un archivo de documento en un servidor que implementa [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="51c41-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51c41-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="51c41-106">Associated properties</span></span>  <br/> |<span data-ttu-id="51c41-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="51c41-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="51c41-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="51c41-108">Property set:</span></span>  <br/> |<span data-ttu-id="51c41-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="51c41-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="51c41-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="51c41-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51c41-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="51c41-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="51c41-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="51c41-112">Data type:</span></span>  <br/> |<span data-ttu-id="51c41-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51c41-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51c41-114">Área:</span><span class="sxs-lookup"><span data-stu-id="51c41-114">Area:</span></span>  <br/> |<span data-ttu-id="51c41-115">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="51c41-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c41-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51c41-116">Remarks</span></span>

<span data-ttu-id="51c41-117">En la tabla siguiente se muestran los valores posibles de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="51c41-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="51c41-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="51c41-118">**Value**</span></span>|<span data-ttu-id="51c41-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51c41-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51c41-120">0</span><span class="sxs-lookup"><span data-stu-id="51c41-120">0</span></span>  <br/> |<span data-ttu-id="51c41-121">El documento no está desproteido.</span><span class="sxs-lookup"><span data-stu-id="51c41-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="51c41-122">1 </span><span class="sxs-lookup"><span data-stu-id="51c41-122">1</span></span>  <br/> |<span data-ttu-id="51c41-123">El documento se desproteme para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="51c41-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="51c41-124">2 </span><span class="sxs-lookup"><span data-stu-id="51c41-124">2</span></span>  <br/> |<span data-ttu-id="51c41-125">El documento no está desprotegiendo, pero el usuario actual tiene una copia del archivo guardado para su edición en el equipo actual.</span><span class="sxs-lookup"><span data-stu-id="51c41-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="51c41-126">Esta propiedad se calcula localmente y no se envía a un servidor en ningún momento a menos que un usuario arrastre el elemento a otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="51c41-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="51c41-127">En ese caso, se trata como una propiedad personalizada definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="51c41-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51c41-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="51c41-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51c41-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="51c41-129">Protocol specifications</span></span>

<span data-ttu-id="51c41-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="51c41-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="51c41-131">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="51c41-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51c41-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="51c41-132">Header files</span></span>

<span data-ttu-id="51c41-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51c41-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="51c41-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="51c41-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51c41-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51c41-135">See also</span></span>



[<span data-ttu-id="51c41-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="51c41-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51c41-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="51c41-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51c41-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="51c41-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51c41-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="51c41-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

