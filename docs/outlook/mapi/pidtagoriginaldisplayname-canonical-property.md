---
title: Propiedad canónica PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355611"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="ab74e-103">Propiedad canónica PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ab74e-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="ab74e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab74e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab74e-105">Contiene el nombre para mostrar original de una entrada copiada de una libreta de direcciones a una libreta de direcciones personal u otra libreta de direcciones grabable.</span><span class="sxs-lookup"><span data-stu-id="ab74e-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab74e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ab74e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab74e-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="ab74e-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="ab74e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ab74e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab74e-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="ab74e-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="ab74e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ab74e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab74e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab74e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab74e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ab74e-112">Area:</span></span>  <br/> |<span data-ttu-id="ab74e-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="ab74e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab74e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab74e-114">Remarks</span></span>

<span data-ttu-id="ab74e-115">Estas propiedades contienen información sobre el origen original de una entrada copiada.</span><span class="sxs-lookup"><span data-stu-id="ab74e-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="ab74e-116">Para un informe no leído, estas propiedades contienen una copia del nombre para mostrar del destinatario del mensaje original para el que se genera el informe.</span><span class="sxs-lookup"><span data-stu-id="ab74e-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="ab74e-117">Cuando el destinatario original forma parte de una lista de distribución, el nombre para mostrar de la lista de distribución se conserva para el informe.</span><span class="sxs-lookup"><span data-stu-id="ab74e-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="ab74e-118">Una aplicación cliente puede usar estas propiedades para evitar la alteración o "suplantación" de entradas, al dar una copia sin modificar del nombre para mostrar para comparar.</span><span class="sxs-lookup"><span data-stu-id="ab74e-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ab74e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab74e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab74e-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ab74e-120">Protocol specifications</span></span>

<span data-ttu-id="ab74e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab74e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab74e-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ab74e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab74e-123">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab74e-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab74e-124">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="ab74e-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab74e-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ab74e-125">Header files</span></span>

<span data-ttu-id="ab74e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab74e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab74e-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ab74e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab74e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab74e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ab74e-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ab74e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab74e-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab74e-130">See also</span></span>



[<span data-ttu-id="ab74e-131">Propiedad canónica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="ab74e-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="ab74e-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ab74e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab74e-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ab74e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab74e-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ab74e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab74e-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ab74e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

