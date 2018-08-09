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
ms.openlocfilehash: df2fa19656aa1bff810a082cda94a091e2c7fc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819675"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="51bf5-103">Propiedad canónica PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="51bf5-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="51bf5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51bf5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51bf5-105">Contiene una marca que indica que un mensaje se ha de lectura, pero no está marcado como leído.</span><span class="sxs-lookup"><span data-stu-id="51bf5-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51bf5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="51bf5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51bf5-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="51bf5-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="51bf5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="51bf5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51bf5-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="51bf5-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="51bf5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="51bf5-110">Data type:</span></span>  <br/> |<span data-ttu-id="51bf5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51bf5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51bf5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="51bf5-112">Area:</span></span>  <br/> |<span data-ttu-id="51bf5-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="51bf5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51bf5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51bf5-114">Remarks</span></span>

<span data-ttu-id="51bf5-115">Esta propiedad se usa en la carpeta de búsqueda de mensajes no leídos de Outlook para realizar un seguimiento de los mensajes que se han leído sin realmente los marcar como leído, que debería quitarlos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="51bf5-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="51bf5-116">Cuando los cambios de la vista se ha quitado esta propiedad y el elemento se marca como de lectura.</span><span class="sxs-lookup"><span data-stu-id="51bf5-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="51bf5-117">Esta propiedad no se sincronizará con el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="51bf5-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51bf5-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="51bf5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51bf5-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="51bf5-119">Protocol specifications</span></span>

<span data-ttu-id="51bf5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51bf5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51bf5-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="51bf5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51bf5-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51bf5-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51bf5-123">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="51bf5-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51bf5-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="51bf5-124">Header files</span></span>

<span data-ttu-id="51bf5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51bf5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="51bf5-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="51bf5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="51bf5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51bf5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="51bf5-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="51bf5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51bf5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="51bf5-129">See also</span></span>



[<span data-ttu-id="51bf5-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="51bf5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51bf5-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="51bf5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51bf5-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="51bf5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51bf5-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="51bf5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

