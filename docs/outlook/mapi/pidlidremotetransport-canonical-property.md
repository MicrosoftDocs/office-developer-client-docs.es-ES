---
title: Propiedad canónica PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439446"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="df908-103">Propiedad canónica PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="df908-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="df908-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df908-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df908-105">Identifica la cuenta con la que está asociado el elemento de encabezado, principalmente para implementar la funcionalidad pop Leave on Server.</span><span class="sxs-lookup"><span data-stu-id="df908-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df908-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="df908-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="df908-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="df908-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="df908-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="df908-108">Property set:</span></span>  <br/> |<span data-ttu-id="df908-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="df908-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="df908-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="df908-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="df908-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="df908-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="df908-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="df908-112">Data type:</span></span>  <br/> |<span data-ttu-id="df908-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="df908-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="df908-114">Área:</span><span class="sxs-lookup"><span data-stu-id="df908-114">Area:</span></span>  <br/> |<span data-ttu-id="df908-115">Mensaje remoto</span><span class="sxs-lookup"><span data-stu-id="df908-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df908-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df908-116">Remarks</span></span>

<span data-ttu-id="df908-117">Esta propiedad solo es relevante en los mensajes que tienen una clase de mensaje de IPM. Remoto.</span><span class="sxs-lookup"><span data-stu-id="df908-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="df908-118">Microsoft Outlook mantiene una asignación de varias cuentas que se descargan en un almacén determinado en un mensaje de información asociada a carpetas (FAI), pero también podría mantener esta información en el Registro.</span><span class="sxs-lookup"><span data-stu-id="df908-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="df908-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="df908-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df908-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="df908-120">Protocol specifications</span></span>

<span data-ttu-id="df908-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="df908-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="df908-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="df908-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df908-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="df908-123">Header files</span></span>

<span data-ttu-id="df908-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df908-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="df908-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="df908-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df908-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df908-126">See also</span></span>



[<span data-ttu-id="df908-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="df908-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df908-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="df908-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df908-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="df908-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df908-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="df908-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

