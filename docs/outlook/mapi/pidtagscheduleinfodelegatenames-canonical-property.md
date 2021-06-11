---
title: Propiedad canónica PidTagScheduleInfoDelegateNames
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314941"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="a39e3-103">Propiedad canónica PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="a39e3-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="a39e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a39e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a39e3-105">Contiene los nombres de los delegados.</span><span class="sxs-lookup"><span data-stu-id="a39e3-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a39e3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a39e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a39e3-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="a39e3-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="a39e3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a39e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a39e3-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="a39e3-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="a39e3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a39e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="a39e3-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a39e3-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a39e3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a39e3-112">Area:</span></span>  <br/> |<span data-ttu-id="a39e3-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="a39e3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a39e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a39e3-114">Remarks</span></span>

<span data-ttu-id="a39e3-115">Cada entrada de estas propiedades debe contener el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones de cada delegado.</span><span class="sxs-lookup"><span data-stu-id="a39e3-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a39e3-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a39e3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a39e3-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a39e3-117">Protocol specifications</span></span>

<span data-ttu-id="a39e3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a39e3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a39e3-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a39e3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a39e3-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a39e3-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a39e3-121">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a39e3-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a39e3-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a39e3-122">Header files</span></span>

<span data-ttu-id="a39e3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a39e3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a39e3-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a39e3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a39e3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a39e3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a39e3-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a39e3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a39e3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a39e3-127">See also</span></span>



[<span data-ttu-id="a39e3-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a39e3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a39e3-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a39e3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a39e3-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a39e3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a39e3-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a39e3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

