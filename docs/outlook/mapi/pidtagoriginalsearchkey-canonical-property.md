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
ms.openlocfilehash: 26854b640669bbc6479ce90ba9cad18cdf4d9264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819851"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="410f1-103">Propiedad canónica PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="410f1-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="410f1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="410f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="410f1-105">Contiene la clave de búsqueda original de una entrada copiada de otra libreta de direcciones grabable o de una libreta de direcciones a una libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="410f1-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="410f1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="410f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="410f1-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="410f1-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="410f1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="410f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="410f1-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="410f1-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="410f1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="410f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="410f1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="410f1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="410f1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="410f1-112">Area:</span></span>  <br/> |<span data-ttu-id="410f1-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="410f1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="410f1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="410f1-114">Remarks</span></span>

<span data-ttu-id="410f1-115">Esta propiedad es una de las propiedades que contienen información sobre el origen original de una entrada de copiado.</span><span class="sxs-lookup"><span data-stu-id="410f1-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="410f1-116">Para un informe nonread, esta propiedad contiene una copia de la clave de búsqueda del destinatario del mensaje original para la que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="410f1-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="410f1-117">Cuando el destinatario original forma parte de una lista de distribución, se conserva la clave de búsqueda de la lista de distribución para el informe.</span><span class="sxs-lookup"><span data-stu-id="410f1-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="410f1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="410f1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="410f1-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="410f1-119">Protocol specifications</span></span>

<span data-ttu-id="410f1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="410f1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="410f1-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="410f1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="410f1-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="410f1-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="410f1-123">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="410f1-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="410f1-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="410f1-124">Header files</span></span>

<span data-ttu-id="410f1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="410f1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="410f1-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="410f1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="410f1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="410f1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="410f1-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="410f1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="410f1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="410f1-129">See also</span></span>



[<span data-ttu-id="410f1-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="410f1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="410f1-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="410f1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="410f1-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="410f1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="410f1-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="410f1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

