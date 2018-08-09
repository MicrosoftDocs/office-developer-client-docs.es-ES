---
title: Propiedad canónica PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819423"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="7d448-103">Propiedad canónica PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="7d448-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7d448-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d448-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d448-105">Contiene el identificador de entrada de la vista predeterminada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7d448-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d448-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7d448-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d448-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7d448-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7d448-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d448-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d448-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="7d448-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="7d448-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7d448-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d448-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d448-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7d448-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d448-112">Area:</span></span>  <br/> |<span data-ttu-id="7d448-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="7d448-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d448-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d448-114">Remarks</span></span>

<span data-ttu-id="7d448-115">Esta propiedad es el identificador de entrada de la vista de carpeta que se debe establecer como la vista inicial.</span><span class="sxs-lookup"><span data-stu-id="7d448-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="7d448-116">No se necesita establecer la propiedad si la vista de "Normal" es que se utilizará como la vista inicial.</span><span class="sxs-lookup"><span data-stu-id="7d448-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="7d448-117">Una aplicación cliente puede obtener esta propiedad en el momento en que se abre la carpeta y mejorar el rendimiento significativo.</span><span class="sxs-lookup"><span data-stu-id="7d448-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="7d448-118">Esta propiedad puede usarse como un acceso directo para obtener la vista predeterminada, en lugar de abrir la tabla de contenido asociado y envío de una restricción.</span><span class="sxs-lookup"><span data-stu-id="7d448-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="7d448-119">Implementación de un proveedor de servicio del método [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) puede copiar esta propiedad cuando copian las carpetas.</span><span class="sxs-lookup"><span data-stu-id="7d448-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d448-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d448-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d448-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d448-121">Protocol specifications</span></span>

<span data-ttu-id="7d448-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d448-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d448-123">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7d448-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d448-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7d448-124">Header files</span></span>

<span data-ttu-id="7d448-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d448-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d448-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7d448-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d448-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d448-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7d448-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="7d448-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d448-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d448-129">See also</span></span>



[<span data-ttu-id="7d448-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d448-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d448-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7d448-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d448-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7d448-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d448-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7d448-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

