---
title: Propiedad canónico PidLidSharingRemoteType
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 8a9975090a8b90946482fa77fd2dafdb503c1f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818926"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="f130b-103">Propiedad canónico PidLidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="f130b-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="f130b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f130b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f130b-105">Especifica el tipo de la carpeta compartida remota.</span><span class="sxs-lookup"><span data-stu-id="f130b-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="f130b-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="f130b-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f130b-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f130b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f130b-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="f130b-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="f130b-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f130b-109">Property set:</span></span>  <br/> |<span data-ttu-id="f130b-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="f130b-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="f130b-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f130b-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f130b-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="f130b-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="f130b-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f130b-113">Data type:</span></span>  <br/> |<span data-ttu-id="f130b-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f130b-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f130b-115">Área:</span><span class="sxs-lookup"><span data-stu-id="f130b-115">Area:</span></span>  <br/> |<span data-ttu-id="f130b-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="f130b-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f130b-117">Notas</span><span class="sxs-lookup"><span data-stu-id="f130b-117">Remarks</span></span>

<span data-ttu-id="f130b-118">Esta propiedad se debe establecer en el mismo valor que la propiedad **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="f130b-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f130b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f130b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f130b-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f130b-120">Protocol specifications</span></span>

<span data-ttu-id="f130b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f130b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f130b-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f130b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f130b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f130b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f130b-124">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="f130b-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f130b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f130b-125">Header files</span></span>

<span data-ttu-id="f130b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f130b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f130b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f130b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f130b-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="f130b-128">See also</span></span>



[<span data-ttu-id="f130b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f130b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f130b-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f130b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f130b-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="f130b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f130b-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f130b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

