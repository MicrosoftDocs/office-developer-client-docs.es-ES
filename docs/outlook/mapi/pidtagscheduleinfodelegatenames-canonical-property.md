---
title: Propiedad canónico PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fed2b23680cd2654bbb6960e3c6be07074307a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820200"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="452c9-103">Propiedad canónico PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="452c9-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="452c9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="452c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="452c9-105">Contiene los nombres de los delegados.</span><span class="sxs-lookup"><span data-stu-id="452c9-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="452c9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="452c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="452c9-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="452c9-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="452c9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="452c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="452c9-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="452c9-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="452c9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="452c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="452c9-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="452c9-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="452c9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="452c9-112">Area:</span></span>  <br/> |<span data-ttu-id="452c9-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="452c9-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="452c9-114">Notas</span><span class="sxs-lookup"><span data-stu-id="452c9-114">Remarks</span></span>

<span data-ttu-id="452c9-115">Cada entrada de estas propiedades debe contener el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones de cada delegado.</span><span class="sxs-lookup"><span data-stu-id="452c9-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="452c9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="452c9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="452c9-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="452c9-117">Protocol specifications</span></span>

<span data-ttu-id="452c9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="452c9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="452c9-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="452c9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="452c9-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="452c9-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="452c9-121">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="452c9-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="452c9-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="452c9-122">Header files</span></span>

<span data-ttu-id="452c9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="452c9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="452c9-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="452c9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="452c9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="452c9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="452c9-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="452c9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="452c9-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="452c9-127">See also</span></span>



[<span data-ttu-id="452c9-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="452c9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="452c9-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="452c9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="452c9-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="452c9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="452c9-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="452c9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

