---
title: Propiedad canónica PidLidSharingRemoteName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eddcc911653830f63ae4afc564af891d3d7213e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595240"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="9fa3b-103">Propiedad canónica PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="9fa3b-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="9fa3b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fa3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fa3b-105">Especifica el nombre de la carpeta remota que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="9fa3b-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fa3b-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9fa3b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fa3b-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="9fa3b-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="9fa3b-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9fa3b-109">Property set:</span></span>  <br/> |<span data-ttu-id="9fa3b-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="9fa3b-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="9fa3b-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="9fa3b-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9fa3b-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="9fa3b-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="9fa3b-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9fa3b-113">Data type:</span></span>  <br/> |<span data-ttu-id="9fa3b-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9fa3b-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9fa3b-115">Área:</span><span class="sxs-lookup"><span data-stu-id="9fa3b-115">Area:</span></span>  <br/> |<span data-ttu-id="9fa3b-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="9fa3b-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fa3b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fa3b-117">Remarks</span></span>

<span data-ttu-id="9fa3b-118">Esta propiedad debe establecerse en el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la carpeta que se está compartida.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9fa3b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fa3b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9fa3b-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9fa3b-120">Protocol specifications</span></span>

<span data-ttu-id="9fa3b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fa3b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fa3b-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9fa3b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fa3b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fa3b-124">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9fa3b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9fa3b-125">Header files</span></span>

<span data-ttu-id="9fa3b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fa3b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fa3b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fa3b-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9fa3b-128">See also</span></span>



[<span data-ttu-id="9fa3b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa3b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fa3b-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9fa3b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fa3b-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa3b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fa3b-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9fa3b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

