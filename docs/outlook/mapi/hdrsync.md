---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816958"
---
# <a name="hdrsync"></a><span data-ttu-id="c66ac-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="c66ac-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="c66ac-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c66ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c66ac-105">Información para la sincronización de un encabezado de mensaje durante el [estado del encabezado de mensaje de descarga](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="c66ac-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c66ac-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c66ac-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="c66ac-107">Members</span><span class="sxs-lookup"><span data-stu-id="c66ac-107">Members</span></span>

 <span data-ttu-id="c66ac-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="c66ac-108">_pupmsg_</span></span>
  
- <span data-ttu-id="c66ac-109">[out] Información para el encabezado del mensaje actual en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="c66ac-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="c66ac-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="c66ac-110">_feidPar_</span></span>
  
- <span data-ttu-id="c66ac-111">[out] Identificador de entrada para la carpeta principal del elemento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c66ac-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="c66ac-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="c66ac-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="c66ac-113">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="c66ac-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="c66ac-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c66ac-114">_ulFlags_</span></span>
  
- <span data-ttu-id="c66ac-115">[entrada] Indicadores para modificar el comportamiento:</span><span class="sxs-lookup"><span data-stu-id="c66ac-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="c66ac-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c66ac-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="c66ac-117">[entrada] Elemento completo reside en el mismo almacén local como el elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c66ac-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="c66ac-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="c66ac-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="c66ac-119">[entrada] Optimizar las operaciones de copia interno.</span><span class="sxs-lookup"><span data-stu-id="c66ac-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="c66ac-120">Esto podría provocar una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="c66ac-120">This might cause data loss.</span></span> <span data-ttu-id="c66ac-121">Se debe establecer **HSF_LOCAL** .</span><span class="sxs-lookup"><span data-stu-id="c66ac-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="c66ac-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="c66ac-122">HSF_OK</span></span>
    
  - <span data-ttu-id="c66ac-123">[entrada] Sincronización de encabezado fue correcta.</span><span class="sxs-lookup"><span data-stu-id="c66ac-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="c66ac-124">El cliente establece esto después de descargar información desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="c66ac-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="c66ac-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="c66ac-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="c66ac-126">[entrada] El elemento de mensaje completo, incluido el encabezado del mensaje se descarga desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="c66ac-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="c66ac-127">Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="c66ac-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c66ac-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c66ac-128">See also</span></span>



[<span data-ttu-id="c66ac-129">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="c66ac-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c66ac-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="c66ac-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c66ac-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c66ac-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c66ac-132">FEID</span><span class="sxs-lookup"><span data-stu-id="c66ac-132">FEID</span></span>](feid.md)

