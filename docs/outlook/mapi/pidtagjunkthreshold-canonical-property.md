---
title: Propiedad canónica PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7d4337105b2dcae94956f0b1badf66c663467dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565665"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="a3050-103">Propiedad canónica PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="a3050-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="a3050-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3050-105">Agresividad indica el correo entrante se debe enviar a la carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="a3050-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3050-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a3050-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3050-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="a3050-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="a3050-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a3050-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3050-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="a3050-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="a3050-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a3050-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3050-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a3050-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a3050-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a3050-112">Area:</span></span>  <br/> |<span data-ttu-id="a3050-113">Spam</span><span class="sxs-lookup"><span data-stu-id="a3050-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3050-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3050-114">Remarks</span></span>

<span data-ttu-id="a3050-115">Esta propiedad corresponde a la alta / baja / ninguna configuración de filtro.</span><span class="sxs-lookup"><span data-stu-id="a3050-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="a3050-116">Un valor de "0xFFFFFFFF" indica que el filtrado de spam no se debe aplicar, sin embargo, aún se deben aplicar las listas de bloqueados.</span><span class="sxs-lookup"><span data-stu-id="a3050-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="a3050-117">Un valor de "0 x 80000000" indica que todo el correo se spam, excepto los mensajes de remitentes de la lista de remitentes de confianza o se envía a los destinatarios de la lista de destinatarios de confianza.</span><span class="sxs-lookup"><span data-stu-id="a3050-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="a3050-118">Los valores de esto son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3050-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="a3050-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a3050-119">**Value**</span></span>|<span data-ttu-id="a3050-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3050-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3050-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a3050-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="a3050-122">Sin filtrado de spam</span><span class="sxs-lookup"><span data-stu-id="a3050-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="a3050-123">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="a3050-123">0x00000006</span></span>  <br/> |<span data-ttu-id="a3050-124">Filtrado de spam baja</span><span class="sxs-lookup"><span data-stu-id="a3050-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="a3050-125">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a3050-125">0x00000003</span></span>  <br/> |<span data-ttu-id="a3050-126">Filtrado de spam alta</span><span class="sxs-lookup"><span data-stu-id="a3050-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="a3050-127">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="a3050-127">0x80000000</span></span>  <br/> |<span data-ttu-id="a3050-128">Sólo listas de confianza</span><span class="sxs-lookup"><span data-stu-id="a3050-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a3050-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3050-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3050-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a3050-130">Protocol specifications</span></span>

<span data-ttu-id="a3050-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3050-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3050-132">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a3050-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3050-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3050-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3050-134">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="a3050-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3050-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a3050-135">Header files</span></span>

<span data-ttu-id="a3050-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3050-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3050-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a3050-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3050-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3050-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a3050-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a3050-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3050-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a3050-140">See also</span></span>



[<span data-ttu-id="a3050-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a3050-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3050-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a3050-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3050-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a3050-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3050-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a3050-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

