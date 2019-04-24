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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342724"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="83815-103">Propiedad canónica PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="83815-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="83815-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83815-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83815-105">Contiene el identificador de entrada original para una entrada copiada de una libreta de direcciones en una libreta personal de direcciones u otra libreta de direcciones grabable.</span><span class="sxs-lookup"><span data-stu-id="83815-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83815-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="83815-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83815-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="83815-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="83815-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="83815-108">Identifier:</span></span>  <br/> |<span data-ttu-id="83815-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="83815-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="83815-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="83815-110">Data type:</span></span>  <br/> |<span data-ttu-id="83815-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="83815-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="83815-112">Área:</span><span class="sxs-lookup"><span data-stu-id="83815-112">Area:</span></span>  <br/> |<span data-ttu-id="83815-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="83815-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83815-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83815-114">Remarks</span></span>

<span data-ttu-id="83815-115">Esta propiedad es una de las propiedades que contienen información sobre el origen original de una entrada que se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="83815-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="83815-116">Para un informe no leído, esta propiedad contiene una copia del identificador de entrada del destinatario del mensaje original para el que se genera el informe.</span><span class="sxs-lookup"><span data-stu-id="83815-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="83815-117">Cuando el destinatario original forma parte de una lista de distribución, el identificador de entrada de la lista de distribución se conserva para el informe.</span><span class="sxs-lookup"><span data-stu-id="83815-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="83815-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="83815-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83815-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="83815-119">Protocol specifications</span></span>

<span data-ttu-id="83815-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83815-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83815-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="83815-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83815-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83815-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83815-123">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="83815-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="83815-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83815-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83815-125">Controla los datos de objetos de mensajería que se sincronizan entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="83815-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83815-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="83815-126">Header files</span></span>

<span data-ttu-id="83815-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="83815-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="83815-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="83815-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="83815-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="83815-129">Mapitags.h</span></span>
  
> <span data-ttu-id="83815-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="83815-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83815-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="83815-131">See also</span></span>



[<span data-ttu-id="83815-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="83815-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83815-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="83815-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83815-134">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="83815-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83815-135">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="83815-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

