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
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270017"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="e3b6a-103">Propiedad canónica PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="e3b6a-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e3b6a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3b6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3b6a-105">Contiene el identificador de entrada de la vista predeterminada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3b6a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e3b6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3b6a-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e3b6a-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e3b6a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e3b6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3b6a-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="e3b6a-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="e3b6a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e3b6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3b6a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e3b6a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e3b6a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e3b6a-112">Area:</span></span>  <br/> |<span data-ttu-id="e3b6a-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b6a-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3b6a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3b6a-114">Remarks</span></span>

<span data-ttu-id="e3b6a-115">Esta propiedad es el identificador de entrada de la vista de carpeta que debe establecerse como vista inicial.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="e3b6a-116">No es necesario establecer la propiedad si se va a usar la vista "Normal" como vista inicial.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="e3b6a-117">Una aplicación cliente puede obtener esta propiedad en el momento en que abre la carpeta y obtener mejoras significativas en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="e3b6a-118">Esta propiedad se puede usar como acceso directo para obtener la vista predeterminada, en lugar de abrir la tabla de contenido asociada y enviar una restricción.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="e3b6a-119">Una implementación del proveedor de servicios del [método IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) puede copiar esta propiedad cuando copia carpetas.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3b6a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3b6a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3b6a-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e3b6a-121">Protocol specifications</span></span>

<span data-ttu-id="e3b6a-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3b6a-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3b6a-123">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3b6a-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b6a-124">Header files</span></span>

<span data-ttu-id="e3b6a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3b6a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3b6a-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3b6a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3b6a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e3b6a-128">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3b6a-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3b6a-129">See also</span></span>



[<span data-ttu-id="e3b6a-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b6a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3b6a-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b6a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3b6a-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b6a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3b6a-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e3b6a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

