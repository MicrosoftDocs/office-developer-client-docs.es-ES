---
title: Propiedad canónica PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437346"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="d5920-103">Propiedad canónica PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="d5920-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d5920-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5920-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5920-105">Contiene el identificador de entrada de la carpeta de vista común predefinida.</span><span class="sxs-lookup"><span data-stu-id="d5920-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5920-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d5920-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5920-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d5920-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d5920-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d5920-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5920-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="d5920-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="d5920-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d5920-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5920-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d5920-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d5920-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d5920-112">Area:</span></span>  <br/> |<span data-ttu-id="d5920-113">Outlook aplicación</span><span class="sxs-lookup"><span data-stu-id="d5920-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5920-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5920-114">Remarks</span></span>

<span data-ttu-id="d5920-115">La carpeta de vista común contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de vista contiene especificadores definidos por un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d5920-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="d5920-116">Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno almacenado como mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5920-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="d5920-117">Una aplicación cliente puede elegir combinar los dos conjuntos de especificadores y hacer que ambos estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="d5920-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="d5920-118">Para obtener más información sobre las vistas, vea [Ver carpetas](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="d5920-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d5920-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5920-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d5920-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d5920-120">Header files</span></span>

<span data-ttu-id="d5920-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5920-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5920-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d5920-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5920-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d5920-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d5920-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d5920-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5920-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5920-125">See also</span></span>



[<span data-ttu-id="d5920-126">Propiedad canónica PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="d5920-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="d5920-127">Propiedad canónica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="d5920-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="d5920-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d5920-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5920-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d5920-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5920-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d5920-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5920-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d5920-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

