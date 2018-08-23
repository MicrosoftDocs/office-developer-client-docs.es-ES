---
title: Propiedad canónica PidTagScheduleInfoDelegateEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f7521d387fa45c191a67f2a20320fac700baed37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567219"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="c78d7-103">Propiedad canónica PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="c78d7-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="c78d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c78d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c78d7-105">Contiene los **identificadores** de los delegados.</span><span class="sxs-lookup"><span data-stu-id="c78d7-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c78d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c78d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c78d7-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="c78d7-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="c78d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c78d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c78d7-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="c78d7-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="c78d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c78d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="c78d7-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c78d7-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c78d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c78d7-112">Area:</span></span>  <br/> |<span data-ttu-id="c78d7-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="c78d7-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c78d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c78d7-114">Remarks</span></span>

<span data-ttu-id="c78d7-115">Cada entrada debe contener el valor de la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de entrada de la libreta de direcciones de cada delegado.</span><span class="sxs-lookup"><span data-stu-id="c78d7-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="c78d7-116">Esta propiedad se debe establecer en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="c78d7-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c78d7-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c78d7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c78d7-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c78d7-118">Protocol specifications</span></span>

<span data-ttu-id="c78d7-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c78d7-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c78d7-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c78d7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c78d7-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c78d7-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c78d7-122">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c78d7-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c78d7-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c78d7-123">Header files</span></span>

<span data-ttu-id="c78d7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c78d7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c78d7-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c78d7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c78d7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c78d7-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c78d7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c78d7-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c78d7-128">See also</span></span>



[<span data-ttu-id="c78d7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c78d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c78d7-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c78d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c78d7-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c78d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c78d7-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c78d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

