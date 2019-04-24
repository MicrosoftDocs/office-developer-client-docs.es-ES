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
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321297"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="c42b3-103">Propiedad canónica PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="c42b3-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="c42b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c42b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c42b3-105">Contiene los **EntryID** de los delegados.</span><span class="sxs-lookup"><span data-stu-id="c42b3-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c42b3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c42b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c42b3-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="c42b3-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="c42b3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c42b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c42b3-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="c42b3-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="c42b3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c42b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c42b3-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c42b3-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c42b3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c42b3-112">Area:</span></span>  <br/> |<span data-ttu-id="c42b3-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c42b3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c42b3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c42b3-114">Remarks</span></span>

<span data-ttu-id="c42b3-115">Cada entrada debe contener el valor de la \*\*\*\* propiedad "[PidTagEntryId](pidtagentryid-canonical-property.md)" de cada entrada de la libreta de direcciones de cada delegado.</span><span class="sxs-lookup"><span data-stu-id="c42b3-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="c42b3-116">Esta propiedad debe establecerse en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="c42b3-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c42b3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c42b3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c42b3-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c42b3-118">Protocol specifications</span></span>

<span data-ttu-id="c42b3-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c42b3-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c42b3-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c42b3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c42b3-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c42b3-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c42b3-122">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c42b3-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c42b3-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c42b3-123">Header files</span></span>

<span data-ttu-id="c42b3-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c42b3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c42b3-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c42b3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c42b3-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c42b3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c42b3-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c42b3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c42b3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c42b3-128">See also</span></span>



[<span data-ttu-id="c42b3-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c42b3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c42b3-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c42b3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c42b3-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c42b3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c42b3-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c42b3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

