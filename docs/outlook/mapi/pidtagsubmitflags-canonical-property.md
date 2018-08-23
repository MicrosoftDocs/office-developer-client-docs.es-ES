---
title: Propiedad canónica PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563691"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="f3e11-103">Propiedad canónica PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="f3e11-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f3e11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3e11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3e11-105">Contiene una máscara de bits de marcadores que indican los detalles acerca de un envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3e11-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3e11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f3e11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3e11-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f3e11-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f3e11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f3e11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3e11-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="f3e11-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="f3e11-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f3e11-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3e11-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3e11-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3e11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f3e11-112">Area:</span></span>  <br/> |<span data-ttu-id="f3e11-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="f3e11-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e11-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3e11-114">Remarks</span></span>

<span data-ttu-id="f3e11-115">La máscara de bits **PR_SUBMIT_FLAGS** se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f3e11-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="f3e11-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="f3e11-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="f3e11-117">La cola MAPI tiene actualmente el mensaje bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f3e11-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="f3e11-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="f3e11-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="f3e11-119">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="f3e11-119">The message needs preprocessing.</span></span> <span data-ttu-id="f3e11-120">Cuando haya terminado la cola MAPI preprocesamiento este mensaje, debe llamar al método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e11-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="f3e11-121">El proveedor de almacén de mensajes reconoce que la cola de impresión, en lugar de la aplicación cliente, ha llamado **SubmitMessage**, borra el indicador y continúa con el envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3e11-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="f3e11-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3e11-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3e11-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f3e11-123">Protocol specifications</span></span>

<span data-ttu-id="f3e11-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e11-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e11-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f3e11-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3e11-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e11-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e11-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f3e11-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3e11-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f3e11-128">Header files</span></span>

<span data-ttu-id="f3e11-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3e11-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3e11-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f3e11-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3e11-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3e11-131">Mapitags.h</span></span>
  
> <span data-ttu-id="f3e11-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f3e11-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3e11-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f3e11-133">See also</span></span>



[<span data-ttu-id="f3e11-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="f3e11-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="f3e11-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f3e11-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3e11-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f3e11-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3e11-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f3e11-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3e11-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f3e11-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

