---
title: Propiedad canónica PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569095"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="d5565-103">Propiedad canónica PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="d5565-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="d5565-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5565-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5565-105">Proporciona el nombre de tabla (archivos .pst) de almacenamiento personal, que el usuario puede editar, para el cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="d5565-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5565-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d5565-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5565-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="d5565-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="d5565-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d5565-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5565-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="d5565-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="d5565-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d5565-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5565-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5565-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d5565-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d5565-112">Area:</span></span>  <br/> |<span data-ttu-id="d5565-113">Tabla de almacenamiento personal (.pst) interno</span><span class="sxs-lookup"><span data-stu-id="d5565-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5565-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5565-114">Remarks</span></span>

<span data-ttu-id="d5565-115">Si la propiedad **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) se usa en su lugar, se abrirá el cuadro de diálogo de configuración, pero el usuario no podrá editar la ruta de acceso y muchas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="d5565-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d5565-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5565-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5565-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d5565-117">Protocol specifications</span></span>

<span data-ttu-id="d5565-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d5565-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d5565-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d5565-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5565-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d5565-120">Header files</span></span>

<span data-ttu-id="d5565-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5565-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5565-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d5565-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5565-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d5565-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d5565-124">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d5565-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5565-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d5565-125">See also</span></span>



[<span data-ttu-id="d5565-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d5565-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5565-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d5565-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5565-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d5565-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5565-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d5565-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

