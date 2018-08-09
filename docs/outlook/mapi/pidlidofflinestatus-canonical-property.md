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
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818815"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="d956c-103">Propiedad canónica PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="d956c-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="d956c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d956c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d956c-105">Determina el estado de un archivo de documento en un servidor que implementa [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="d956c-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d956c-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="d956c-106">Associated properties</span></span>  <br/> |<span data-ttu-id="d956c-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="d956c-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="d956c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d956c-108">Property set:</span></span>  <br/> |<span data-ttu-id="d956c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d956c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d956c-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d956c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d956c-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="d956c-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="d956c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d956c-112">Data type:</span></span>  <br/> |<span data-ttu-id="d956c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d956c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d956c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d956c-114">Area:</span></span>  <br/> |<span data-ttu-id="d956c-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="d956c-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d956c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d956c-116">Remarks</span></span>

<span data-ttu-id="d956c-117">En la siguiente tabla se muestra los valores posibles de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d956c-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="d956c-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d956c-118">**Value**</span></span>|<span data-ttu-id="d956c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d956c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d956c-120">0</span><span class="sxs-lookup"><span data-stu-id="d956c-120">0</span></span>  <br/> |<span data-ttu-id="d956c-121">Documento no está desprotegido.</span><span class="sxs-lookup"><span data-stu-id="d956c-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="d956c-122">1</span><span class="sxs-lookup"><span data-stu-id="d956c-122">1</span></span>  <br/> |<span data-ttu-id="d956c-123">Documento está desprotegido para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d956c-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="d956c-124">2</span><span class="sxs-lookup"><span data-stu-id="d956c-124">2</span></span>  <br/> |<span data-ttu-id="d956c-125">Documento no está desprotegido, pero el usuario actual tiene una copia del archivo guardado para su edición en el equipo actual.</span><span class="sxs-lookup"><span data-stu-id="d956c-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="d956c-126">Esta propiedad se calcula localmente y no se envía a un servidor en cualquier momento a menos que un usuario arrastra el elemento a otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="d956c-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="d956c-127">En ese caso, se trata como una propiedad personalizada definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d956c-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d956c-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d956c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d956c-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d956c-129">Protocol specifications</span></span>

<span data-ttu-id="d956c-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d956c-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d956c-131">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d956c-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d956c-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d956c-132">Header files</span></span>

<span data-ttu-id="d956c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d956c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="d956c-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d956c-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d956c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d956c-135">See also</span></span>



[<span data-ttu-id="d956c-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d956c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d956c-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d956c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d956c-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d956c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d956c-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d956c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

