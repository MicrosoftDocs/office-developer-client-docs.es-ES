---
title: Propiedad canónica PidLidSharingRemoteType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3297ca951097c9f3601086809c6e294854c88656
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331216"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="bcfe0-103">Propiedad canónica PidLidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="bcfe0-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="bcfe0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcfe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcfe0-105">Especifica el tipo de la carpeta compartida remota.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="bcfe0-106">Esta es una propiedad de un mensaje de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcfe0-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bcfe0-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcfe0-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="bcfe0-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="bcfe0-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="bcfe0-109">Property set:</span></span>  <br/> |<span data-ttu-id="bcfe0-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="bcfe0-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="bcfe0-111">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="bcfe0-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bcfe0-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="bcfe0-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="bcfe0-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bcfe0-113">Data type:</span></span>  <br/> |<span data-ttu-id="bcfe0-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcfe0-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bcfe0-115">Área:</span><span class="sxs-lookup"><span data-stu-id="bcfe0-115">Area:</span></span>  <br/> |<span data-ttu-id="bcfe0-116">Compartir</span><span class="sxs-lookup"><span data-stu-id="bcfe0-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcfe0-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcfe0-117">Remarks</span></span>

<span data-ttu-id="bcfe0-118">Esta propiedad debe establecerse en el mismo valor que la propiedad **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcfe0-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcfe0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcfe0-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="bcfe0-120">Protocol specifications</span></span>

<span data-ttu-id="bcfe0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfe0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfe0-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcfe0-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfe0-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfe0-124">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcfe0-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bcfe0-125">Header files</span></span>

<span data-ttu-id="bcfe0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcfe0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcfe0-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcfe0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcfe0-128">See also</span></span>



[<span data-ttu-id="bcfe0-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcfe0-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcfe0-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcfe0-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="bcfe0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

