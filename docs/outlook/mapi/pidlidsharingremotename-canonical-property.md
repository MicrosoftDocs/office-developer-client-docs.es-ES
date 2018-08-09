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
ms.openlocfilehash: fc3324cb686733f06b9cc0945c93b7df2e5980ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818925"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="b11b4-103">Propiedad canónica PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="b11b4-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="b11b4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b11b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b11b4-105">Especifica el nombre de la carpeta remota que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="b11b4-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="b11b4-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="b11b4-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b11b4-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b11b4-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b11b4-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="b11b4-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="b11b4-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b11b4-109">Property set:</span></span>  <br/> |<span data-ttu-id="b11b4-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="b11b4-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="b11b4-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="b11b4-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b11b4-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="b11b4-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="b11b4-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b11b4-113">Data type:</span></span>  <br/> |<span data-ttu-id="b11b4-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b11b4-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b11b4-115">Área:</span><span class="sxs-lookup"><span data-stu-id="b11b4-115">Area:</span></span>  <br/> |<span data-ttu-id="b11b4-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="b11b4-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b11b4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b11b4-117">Remarks</span></span>

<span data-ttu-id="b11b4-118">Esta propiedad debe establecerse en el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la carpeta que se está compartida.</span><span class="sxs-lookup"><span data-stu-id="b11b4-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b11b4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b11b4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b11b4-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b11b4-120">Protocol specifications</span></span>

<span data-ttu-id="b11b4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b11b4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b11b4-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b11b4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b11b4-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b11b4-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b11b4-124">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="b11b4-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b11b4-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b11b4-125">Header files</span></span>

<span data-ttu-id="b11b4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b11b4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b11b4-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b11b4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b11b4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b11b4-128">See also</span></span>



[<span data-ttu-id="b11b4-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b11b4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b11b4-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b11b4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b11b4-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b11b4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b11b4-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b11b4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

