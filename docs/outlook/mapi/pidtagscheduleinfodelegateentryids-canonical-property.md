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
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820207"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="cde34-103">Propiedad canónica PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="cde34-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="cde34-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cde34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cde34-105">Contiene los **identificadores** de los delegados.</span><span class="sxs-lookup"><span data-stu-id="cde34-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cde34-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cde34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cde34-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="cde34-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="cde34-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cde34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cde34-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="cde34-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="cde34-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cde34-110">Data type:</span></span>  <br/> |<span data-ttu-id="cde34-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="cde34-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="cde34-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cde34-112">Area:</span></span>  <br/> |<span data-ttu-id="cde34-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="cde34-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cde34-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cde34-114">Remarks</span></span>

<span data-ttu-id="cde34-115">Cada entrada debe contener el valor de la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de entrada de la libreta de direcciones de cada delegado.</span><span class="sxs-lookup"><span data-stu-id="cde34-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="cde34-116">Esta propiedad se debe establecer en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="cde34-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cde34-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cde34-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cde34-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cde34-118">Protocol specifications</span></span>

<span data-ttu-id="cde34-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cde34-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cde34-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cde34-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cde34-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cde34-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cde34-122">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="cde34-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cde34-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cde34-123">Header files</span></span>

<span data-ttu-id="cde34-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cde34-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cde34-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cde34-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cde34-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cde34-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cde34-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cde34-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cde34-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cde34-128">See also</span></span>



[<span data-ttu-id="cde34-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cde34-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cde34-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cde34-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cde34-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cde34-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cde34-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cde34-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

