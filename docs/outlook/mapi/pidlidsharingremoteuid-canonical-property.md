---
title: Propiedad canónica PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331265"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="29f73-103">Propiedad canónica PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="29f73-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="29f73-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29f73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29f73-105">Especifica el identificador de entrada de la carpeta remota que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="29f73-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="29f73-106">Esta es una propiedad de un mensaje de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="29f73-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29f73-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29f73-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="29f73-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="29f73-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="29f73-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="29f73-109">Property set:</span></span>  <br/> |<span data-ttu-id="29f73-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="29f73-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="29f73-111">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="29f73-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="29f73-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="29f73-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="29f73-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29f73-113">Data type:</span></span>  <br/> |<span data-ttu-id="29f73-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29f73-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29f73-115">Área:</span><span class="sxs-lookup"><span data-stu-id="29f73-115">Area:</span></span>  <br/> |<span data-ttu-id="29f73-116">Compartir</span><span class="sxs-lookup"><span data-stu-id="29f73-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29f73-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29f73-117">Remarks</span></span>

<span data-ttu-id="29f73-118">Esta propiedad debe establecerse en la representación de cadena hexadecimal del valor de la propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la carpeta que se comparte.</span><span class="sxs-lookup"><span data-stu-id="29f73-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="29f73-119">Esta es una propiedad de un mensaje de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="29f73-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="29f73-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29f73-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29f73-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="29f73-121">Protocol specifications</span></span>

<span data-ttu-id="29f73-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29f73-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29f73-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="29f73-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29f73-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29f73-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29f73-125">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="29f73-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29f73-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="29f73-126">Header files</span></span>

<span data-ttu-id="29f73-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29f73-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="29f73-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="29f73-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29f73-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="29f73-129">See also</span></span>



[<span data-ttu-id="29f73-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29f73-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29f73-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="29f73-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29f73-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="29f73-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29f73-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="29f73-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

