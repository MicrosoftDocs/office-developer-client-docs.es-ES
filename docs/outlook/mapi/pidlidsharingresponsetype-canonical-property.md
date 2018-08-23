---
title: Propiedad canónica PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: beb2c46b43ae77de08900aeb987d875e85575aba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563187"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="95a83-103">Propiedad canónica PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="95a83-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="95a83-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95a83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95a83-105">Especifica el tipo de respuesta con el que ha respondido el destinatario de la solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="95a83-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="95a83-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="95a83-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95a83-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="95a83-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="95a83-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="95a83-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="95a83-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="95a83-109">Property set:</span></span>  <br/> |<span data-ttu-id="95a83-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="95a83-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="95a83-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="95a83-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95a83-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="95a83-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="95a83-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="95a83-113">Data type:</span></span>  <br/> |<span data-ttu-id="95a83-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="95a83-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="95a83-115">Área:</span><span class="sxs-lookup"><span data-stu-id="95a83-115">Area:</span></span>  <br/> |<span data-ttu-id="95a83-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="95a83-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a83-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95a83-117">Remarks</span></span>

<span data-ttu-id="95a83-118">El valor de esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="95a83-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="95a83-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="95a83-119">**Value**</span></span>|<span data-ttu-id="95a83-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95a83-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95a83-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95a83-121">0x00000000</span></span>  <br/> |<span data-ttu-id="95a83-122">No hay respuesta</span><span class="sxs-lookup"><span data-stu-id="95a83-122">No response</span></span>  <br/> |
|<span data-ttu-id="95a83-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="95a83-123">0x00000001</span></span>  <br/> |<span data-ttu-id="95a83-124">Aceptado</span><span class="sxs-lookup"><span data-stu-id="95a83-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="95a83-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="95a83-125">0x00000002</span></span>  <br/> |<span data-ttu-id="95a83-126">Denegado</span><span class="sxs-lookup"><span data-stu-id="95a83-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="95a83-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95a83-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95a83-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="95a83-128">Protocol specifications</span></span>

<span data-ttu-id="95a83-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95a83-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95a83-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="95a83-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95a83-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95a83-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95a83-132">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="95a83-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95a83-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="95a83-133">Header files</span></span>

<span data-ttu-id="95a83-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95a83-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="95a83-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="95a83-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95a83-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="95a83-136">See also</span></span>



[<span data-ttu-id="95a83-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95a83-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95a83-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="95a83-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95a83-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="95a83-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95a83-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="95a83-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

