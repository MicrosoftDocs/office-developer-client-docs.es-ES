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
ms.openlocfilehash: 4a43bc33f13d8325a55d09b5ef3031dc632cf587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819813"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="abeea-103">Propiedad canónica PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="abeea-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="abeea-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abeea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="abeea-105">Contiene el nombre para mostrar original para una entrada de copia de una libreta de direcciones a otra libreta de direcciones puede escribir o de una libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="abeea-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abeea-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="abeea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abeea-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="abeea-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="abeea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="abeea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="abeea-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="abeea-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="abeea-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="abeea-110">Data type:</span></span>  <br/> |<span data-ttu-id="abeea-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abeea-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abeea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="abeea-112">Area:</span></span>  <br/> |<span data-ttu-id="abeea-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="abeea-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abeea-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abeea-114">Remarks</span></span>

<span data-ttu-id="abeea-115">Estas propiedades contienen información acerca de la fuente original de una entrada de copiado.</span><span class="sxs-lookup"><span data-stu-id="abeea-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="abeea-116">Para un informe nonread, estas propiedades contienen una copia del nombre para mostrar del destinatario del mensaje original para la que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="abeea-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="abeea-117">Cuando el destinatario original forma parte de una lista de distribución, se mantiene el nombre para mostrar de la lista de distribución para el informe.</span><span class="sxs-lookup"><span data-stu-id="abeea-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="abeea-118">Una aplicación cliente puede usar estas propiedades para evitar la alteración o "suplantación" de entradas, proporcionando una copia sin alterar del nombre para mostrar se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="abeea-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abeea-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="abeea-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abeea-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="abeea-120">Protocol specifications</span></span>

<span data-ttu-id="abeea-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abeea-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abeea-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="abeea-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abeea-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abeea-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abeea-124">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="abeea-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abeea-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="abeea-125">Header files</span></span>

<span data-ttu-id="abeea-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abeea-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abeea-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="abeea-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="abeea-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="abeea-128">Mapitags.h</span></span>
  
> <span data-ttu-id="abeea-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="abeea-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abeea-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="abeea-130">See also</span></span>



[<span data-ttu-id="abeea-131">Propiedad canónica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="abeea-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="abeea-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="abeea-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abeea-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="abeea-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abeea-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="abeea-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abeea-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="abeea-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
