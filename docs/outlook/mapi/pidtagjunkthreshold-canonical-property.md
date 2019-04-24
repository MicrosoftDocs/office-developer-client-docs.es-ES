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
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326855"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="1fab8-103">Propiedad canónica PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="1fab8-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="1fab8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fab8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fab8-105">Indica cómo se debe enviar el correo entrante de forma agresiva a la carpeta de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="1fab8-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1fab8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1fab8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fab8-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="1fab8-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="1fab8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1fab8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fab8-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="1fab8-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="1fab8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1fab8-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fab8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1fab8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1fab8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1fab8-112">Area:</span></span>  <br/> |<span data-ttu-id="1fab8-113">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="1fab8-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fab8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1fab8-114">Remarks</span></span>

<span data-ttu-id="1fab8-115">Esta propiedad corresponde a la configuración de filtro alto/bajo/ninguno.</span><span class="sxs-lookup"><span data-stu-id="1fab8-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="1fab8-116">Un valor de "0xFFFFFFFF" indica que no se debe aplicar el filtrado de correo no deseado; sin embargo, las listas de bloqueo todavía deben aplicarse.</span><span class="sxs-lookup"><span data-stu-id="1fab8-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="1fab8-117">Un valor de "0x80000000" indica que todo el correo es correo no deseado excepto los mensajes de los remitentes de la lista de remitentes de confianza o enviados a los destinatarios de la lista de destinatarios de confianza.</span><span class="sxs-lookup"><span data-stu-id="1fab8-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="1fab8-118">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1fab8-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="1fab8-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="1fab8-119">**Value**</span></span>|<span data-ttu-id="1fab8-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fab8-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fab8-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1fab8-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="1fab8-122">Sin filtrado de correo no deseado</span><span class="sxs-lookup"><span data-stu-id="1fab8-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="1fab8-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="1fab8-123">0x00000006</span></span>  <br/> |<span data-ttu-id="1fab8-124">Filtrado de correo no deseado bajo</span><span class="sxs-lookup"><span data-stu-id="1fab8-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="1fab8-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1fab8-125">0x00000003</span></span>  <br/> |<span data-ttu-id="1fab8-126">Filtrado de correo no deseado alto</span><span class="sxs-lookup"><span data-stu-id="1fab8-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="1fab8-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="1fab8-127">0x80000000</span></span>  <br/> |<span data-ttu-id="1fab8-128">Solo listas de confianza</span><span class="sxs-lookup"><span data-stu-id="1fab8-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1fab8-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fab8-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fab8-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1fab8-130">Protocol specifications</span></span>

<span data-ttu-id="1fab8-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fab8-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fab8-132">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1fab8-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fab8-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fab8-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fab8-134">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="1fab8-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1fab8-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1fab8-135">Header files</span></span>

<span data-ttu-id="1fab8-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1fab8-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fab8-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1fab8-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fab8-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1fab8-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1fab8-139">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1fab8-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fab8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fab8-140">See also</span></span>



[<span data-ttu-id="1fab8-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1fab8-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fab8-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1fab8-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fab8-143">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1fab8-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fab8-144">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1fab8-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

