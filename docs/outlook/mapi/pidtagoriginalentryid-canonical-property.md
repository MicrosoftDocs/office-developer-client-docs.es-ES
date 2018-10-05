---
title: Propiedad canónica PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f3f4f42d91c4091943d6183508e2bc76c17197fa
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391048"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="3b016-103">Propiedad canónica PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="3b016-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3b016-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b016-105">Contiene el identificador de entrada original para una entrada de copiado de otra libreta de direcciones grabable o de una libreta de direcciones a una libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="3b016-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b016-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3b016-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b016-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3b016-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3b016-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3b016-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b016-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="3b016-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="3b016-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3b016-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b016-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b016-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b016-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3b016-112">Area:</span></span>  <br/> |<span data-ttu-id="3b016-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="3b016-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b016-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b016-114">Remarks</span></span>

<span data-ttu-id="3b016-115">Esta propiedad es una de las propiedades que contienen información sobre el origen original de una entrada de copiado.</span><span class="sxs-lookup"><span data-stu-id="3b016-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="3b016-116">Para un informe nonread, esta propiedad contiene una copia del identificador de entrada del destinatario del mensaje original para la que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="3b016-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="3b016-117">Cuando el destinatario original forma parte de una lista de distribución, se conserva el identificador de entrada de la lista de distribución para el informe.</span><span class="sxs-lookup"><span data-stu-id="3b016-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b016-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b016-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b016-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3b016-119">Protocol specifications</span></span>

<span data-ttu-id="3b016-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b016-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b016-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3b016-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b016-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b016-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b016-123">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="3b016-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="3b016-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b016-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b016-125">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="3b016-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b016-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3b016-126">Header files</span></span>

<span data-ttu-id="3b016-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b016-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b016-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3b016-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b016-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b016-129">Mapitags.h</span></span>
  
> <span data-ttu-id="3b016-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3b016-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b016-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b016-131">See also</span></span>



[<span data-ttu-id="3b016-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3b016-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b016-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3b016-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b016-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3b016-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b016-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3b016-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

