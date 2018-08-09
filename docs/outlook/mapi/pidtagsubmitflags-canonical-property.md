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
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820369"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="0e366-103">Propiedad canónica PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="0e366-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0e366-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e366-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e366-105">Contiene una máscara de bits de marcadores que indican los detalles acerca de un envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0e366-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e366-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0e366-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e366-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0e366-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0e366-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e366-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e366-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="0e366-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="0e366-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0e366-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e366-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e366-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e366-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e366-112">Area:</span></span>  <br/> |<span data-ttu-id="0e366-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="0e366-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e366-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e366-114">Remarks</span></span>

<span data-ttu-id="0e366-115">La máscara de bits **PR_SUBMIT_FLAGS** se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="0e366-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="0e366-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="0e366-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="0e366-117">La cola MAPI tiene actualmente el mensaje bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0e366-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="0e366-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="0e366-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="0e366-119">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="0e366-119">The message needs preprocessing.</span></span> <span data-ttu-id="0e366-120">Cuando haya terminado la cola MAPI preprocesamiento este mensaje, debe llamar al método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="0e366-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="0e366-121">El proveedor de almacén de mensajes reconoce que la cola de impresión, en lugar de la aplicación cliente, ha llamado **SubmitMessage**, borra el indicador y continúa con el envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0e366-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0e366-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e366-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e366-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0e366-123">Protocol specifications</span></span>

<span data-ttu-id="0e366-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e366-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e366-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0e366-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e366-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e366-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e366-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="0e366-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e366-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0e366-128">Header files</span></span>

<span data-ttu-id="0e366-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e366-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e366-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0e366-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e366-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e366-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0e366-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e366-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e366-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e366-133">See also</span></span>



[<span data-ttu-id="0e366-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="0e366-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="0e366-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e366-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e366-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0e366-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e366-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0e366-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e366-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0e366-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

