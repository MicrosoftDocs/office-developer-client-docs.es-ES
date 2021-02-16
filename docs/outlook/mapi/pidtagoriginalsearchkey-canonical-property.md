---
title: Propiedad canónica PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355296"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="ea823-103">Propiedad canónica PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="ea823-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ea823-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea823-105">Contiene la clave de búsqueda original de una entrada copiada de una libreta de direcciones a una libreta de direcciones personal u otra libreta de direcciones que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="ea823-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea823-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ea823-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea823-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ea823-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ea823-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ea823-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea823-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="ea823-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="ea823-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ea823-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea823-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ea823-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ea823-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ea823-112">Area:</span></span>  <br/> |<span data-ttu-id="ea823-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="ea823-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea823-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea823-114">Remarks</span></span>

<span data-ttu-id="ea823-115">Esta propiedad es una de las propiedades que contienen información sobre el origen original de una entrada copiada.</span><span class="sxs-lookup"><span data-stu-id="ea823-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="ea823-116">Para un informe no leído, esta propiedad contiene una copia de la clave de búsqueda del destinatario del mensaje original para el que se genera el informe.</span><span class="sxs-lookup"><span data-stu-id="ea823-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="ea823-117">Cuando el destinatario original forma parte de una lista de distribución, la clave de búsqueda de la lista de distribución se conserva para el informe.</span><span class="sxs-lookup"><span data-stu-id="ea823-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea823-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea823-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea823-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ea823-119">Protocol specifications</span></span>

<span data-ttu-id="ea823-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea823-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea823-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ea823-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea823-122">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea823-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea823-123">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="ea823-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea823-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ea823-124">Header files</span></span>

<span data-ttu-id="ea823-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea823-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea823-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ea823-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea823-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea823-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ea823-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ea823-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea823-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea823-129">See also</span></span>



[<span data-ttu-id="ea823-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ea823-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea823-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ea823-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea823-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ea823-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea823-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ea823-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

