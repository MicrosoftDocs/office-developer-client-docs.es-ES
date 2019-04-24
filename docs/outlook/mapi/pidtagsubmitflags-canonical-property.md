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
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339357"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="ca876-103">Propiedad canónica PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="ca876-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ca876-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca876-105">Contiene una máscara de transmisión de marcas que indican detalles sobre el envío de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca876-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca876-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ca876-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca876-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ca876-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ca876-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ca876-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca876-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="ca876-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="ca876-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ca876-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca876-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ca876-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ca876-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ca876-112">Area:</span></span>  <br/> |<span data-ttu-id="ca876-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="ca876-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca876-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca876-114">Remarks</span></span>

<span data-ttu-id="ca876-115">Se pueden configurar uno o varios de los siguientes indicadores para la máscara de **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="ca876-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="ca876-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="ca876-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="ca876-117">La cola MAPI tiene bloqueado el mensaje en ese momento.</span><span class="sxs-lookup"><span data-stu-id="ca876-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="ca876-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="ca876-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="ca876-119">El mensaje necesita preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="ca876-119">The message needs preprocessing.</span></span> <span data-ttu-id="ca876-120">Cuando la cola MAPI ha terminado de procesar el mensaje, debe llamar al método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ca876-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="ca876-121">El proveedor de almacén de mensajes reconoce que la cola de impresión, en lugar de la aplicación cliente, ha llamado a **SubmitMessage**, borra la marca y sigue el envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca876-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ca876-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca876-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca876-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ca876-123">Protocol specifications</span></span>

<span data-ttu-id="ca876-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca876-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca876-125">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ca876-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca876-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca876-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca876-127">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="ca876-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca876-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ca876-128">Header files</span></span>

<span data-ttu-id="ca876-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ca876-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca876-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ca876-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca876-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ca876-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ca876-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ca876-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca876-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca876-133">See also</span></span>



[<span data-ttu-id="ca876-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="ca876-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="ca876-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ca876-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca876-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ca876-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca876-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ca876-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca876-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ca876-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

