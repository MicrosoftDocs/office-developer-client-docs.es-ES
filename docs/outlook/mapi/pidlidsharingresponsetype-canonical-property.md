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
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331195"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="f0922-103">Propiedad canónica PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="f0922-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="f0922-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0922-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0922-105">Especifica el tipo de respuesta con el que responde el destinatario de la solicitud de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="f0922-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="f0922-106">Se trata de una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="f0922-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0922-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f0922-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0922-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="f0922-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="f0922-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f0922-109">Property set:</span></span>  <br/> |<span data-ttu-id="f0922-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="f0922-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="f0922-111">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="f0922-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f0922-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="f0922-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="f0922-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f0922-113">Data type:</span></span>  <br/> |<span data-ttu-id="f0922-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f0922-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f0922-115">Área:</span><span class="sxs-lookup"><span data-stu-id="f0922-115">Area:</span></span>  <br/> |<span data-ttu-id="f0922-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="f0922-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0922-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0922-117">Remarks</span></span>

<span data-ttu-id="f0922-118">El valor de esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f0922-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="f0922-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="f0922-119">**Value**</span></span>|<span data-ttu-id="f0922-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0922-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0922-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0922-121">0x00000000</span></span>  <br/> |<span data-ttu-id="f0922-122">Sin respuesta</span><span class="sxs-lookup"><span data-stu-id="f0922-122">No response</span></span>  <br/> |
|<span data-ttu-id="f0922-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f0922-123">0x00000001</span></span>  <br/> |<span data-ttu-id="f0922-124">Aceptadas</span><span class="sxs-lookup"><span data-stu-id="f0922-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="f0922-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f0922-125">0x00000002</span></span>  <br/> |<span data-ttu-id="f0922-126">Denegado</span><span class="sxs-lookup"><span data-stu-id="f0922-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f0922-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0922-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0922-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f0922-128">Protocol specifications</span></span>

<span data-ttu-id="f0922-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0922-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0922-130">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f0922-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0922-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0922-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0922-132">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="f0922-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0922-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f0922-133">Header files</span></span>

<span data-ttu-id="f0922-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f0922-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0922-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f0922-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0922-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0922-136">See also</span></span>



[<span data-ttu-id="f0922-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f0922-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0922-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f0922-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0922-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f0922-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0922-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f0922-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

