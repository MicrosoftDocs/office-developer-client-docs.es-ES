---
title: Propiedad canónica PidLidSharingInitiatorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336851"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="79ff5-103">Propiedad canónica PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="79ff5-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="79ff5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79ff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79ff5-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="79ff5-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79ff5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="79ff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79ff5-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="79ff5-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="79ff5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="79ff5-108">Property set:</span></span>  <br/> |<span data-ttu-id="79ff5-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="79ff5-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="79ff5-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="79ff5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="79ff5-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="79ff5-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="79ff5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="79ff5-112">Data type:</span></span>  <br/> |<span data-ttu-id="79ff5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="79ff5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="79ff5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="79ff5-114">Area:</span></span>  <br/> |<span data-ttu-id="79ff5-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="79ff5-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79ff5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79ff5-116">Remarks</span></span>

<span data-ttu-id="79ff5-117">Esta propiedad debe establecerse en el valor de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones identificada por **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) y debe pasarse por alto.</span><span class="sxs-lookup"><span data-stu-id="79ff5-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="79ff5-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="79ff5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79ff5-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="79ff5-119">Protocol specifications</span></span>

<span data-ttu-id="79ff5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79ff5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79ff5-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="79ff5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79ff5-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79ff5-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79ff5-123">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="79ff5-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79ff5-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="79ff5-124">Header files</span></span>

<span data-ttu-id="79ff5-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="79ff5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="79ff5-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="79ff5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79ff5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="79ff5-127">See also</span></span>



[<span data-ttu-id="79ff5-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="79ff5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79ff5-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="79ff5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79ff5-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="79ff5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79ff5-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="79ff5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

