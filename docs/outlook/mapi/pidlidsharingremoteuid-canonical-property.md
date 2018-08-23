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
ms.openlocfilehash: cd42711fc5647f16b33677a330e71d141f1962d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566869"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="07863-103">Propiedad canónica PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="07863-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="07863-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07863-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07863-105">Especifica el identificador de entrada de la carpeta remota que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="07863-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="07863-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="07863-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07863-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="07863-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="07863-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="07863-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="07863-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="07863-109">Property set:</span></span>  <br/> |<span data-ttu-id="07863-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="07863-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="07863-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="07863-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="07863-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="07863-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="07863-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="07863-113">Data type:</span></span>  <br/> |<span data-ttu-id="07863-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07863-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="07863-115">Área:</span><span class="sxs-lookup"><span data-stu-id="07863-115">Area:</span></span>  <br/> |<span data-ttu-id="07863-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="07863-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07863-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07863-117">Remarks</span></span>

<span data-ttu-id="07863-118">Esta propiedad debe establecerse en la representación de cadena hexadecimal del valor de la propiedad de entrada del objeto ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la carpeta que se está compartida.</span><span class="sxs-lookup"><span data-stu-id="07863-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="07863-119">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="07863-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07863-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07863-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07863-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="07863-121">Protocol specifications</span></span>

<span data-ttu-id="07863-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07863-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07863-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="07863-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07863-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07863-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07863-125">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="07863-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07863-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="07863-126">Header files</span></span>

<span data-ttu-id="07863-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07863-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="07863-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="07863-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07863-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="07863-129">See also</span></span>



[<span data-ttu-id="07863-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07863-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07863-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="07863-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07863-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="07863-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07863-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="07863-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

