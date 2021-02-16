---
title: Propiedad canónica PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357704"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="da37f-103">Propiedad canónica PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="da37f-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="da37f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da37f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da37f-105">Contiene una marca que indica que un mensaje se ha leído, pero no se ha marcado como leído.</span><span class="sxs-lookup"><span data-stu-id="da37f-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da37f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="da37f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da37f-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="da37f-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="da37f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="da37f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da37f-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="da37f-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="da37f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="da37f-110">Data type:</span></span>  <br/> |<span data-ttu-id="da37f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da37f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da37f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="da37f-112">Area:</span></span>  <br/> |<span data-ttu-id="da37f-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="da37f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da37f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da37f-114">Remarks</span></span>

<span data-ttu-id="da37f-115">Esta propiedad se usa en la carpeta de búsqueda Mensajes no leídos de Outlook para realizar un seguimiento de los mensajes que se han leído sin marcarlos realmente como leídos, lo que los quitaría de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="da37f-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="da37f-116">Cuando la vista cambia, esta propiedad se quita y el elemento se marca como leído.</span><span class="sxs-lookup"><span data-stu-id="da37f-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="da37f-117">Esta propiedad no se sincronizará con el Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="da37f-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="da37f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="da37f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da37f-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="da37f-119">Protocol specifications</span></span>

<span data-ttu-id="da37f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da37f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da37f-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="da37f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da37f-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da37f-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da37f-123">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="da37f-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da37f-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="da37f-124">Header files</span></span>

<span data-ttu-id="da37f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da37f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="da37f-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="da37f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="da37f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da37f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="da37f-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="da37f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da37f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da37f-129">See also</span></span>



[<span data-ttu-id="da37f-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="da37f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da37f-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="da37f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da37f-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="da37f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da37f-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="da37f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

