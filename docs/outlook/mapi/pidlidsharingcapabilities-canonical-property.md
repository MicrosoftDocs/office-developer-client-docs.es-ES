---
title: Propiedad canónico PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 73f39c0b97ebcd5c84bb908b62f758eaacd4eabf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818904"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="99263-103">Propiedad canónico PidLidSharingCapabilities</span><span class="sxs-lookup"><span data-stu-id="99263-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="99263-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99263-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99263-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="99263-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99263-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="99263-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99263-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="99263-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="99263-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="99263-108">Property set:</span></span>  <br/> |<span data-ttu-id="99263-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="99263-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="99263-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="99263-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99263-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="99263-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="99263-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="99263-112">Data type:</span></span>  <br/> |<span data-ttu-id="99263-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="99263-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="99263-114">Área:</span><span class="sxs-lookup"><span data-stu-id="99263-114">Area:</span></span>  <br/> |<span data-ttu-id="99263-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="99263-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99263-116">Notas</span><span class="sxs-lookup"><span data-stu-id="99263-116">Remarks</span></span>

<span data-ttu-id="99263-117">Esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="99263-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="99263-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="99263-118">**Value**</span></span>|<span data-ttu-id="99263-119">**Escenario**</span><span class="sxs-lookup"><span data-stu-id="99263-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99263-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="99263-120">0x00040290</span></span>  <br/> |<span data-ttu-id="99263-121">Este objeto de mensaje de uso compartido está relacionado con una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="99263-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="99263-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="99263-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="99263-123">Este objeto de mensaje de uso compartido de no estar relacionado con una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="99263-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="99263-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="99263-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99263-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="99263-125">Protocol specifications</span></span>

<span data-ttu-id="99263-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99263-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99263-127">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="99263-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99263-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99263-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99263-129">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="99263-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99263-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="99263-130">Header files</span></span>

<span data-ttu-id="99263-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99263-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="99263-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="99263-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99263-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="99263-133">See also</span></span>



[<span data-ttu-id="99263-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="99263-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99263-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="99263-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99263-136">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="99263-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99263-137">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99263-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

