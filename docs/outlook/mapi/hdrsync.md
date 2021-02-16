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
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410255"
---
# <a name="hdrsync"></a><span data-ttu-id="5068f-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="5068f-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="5068f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5068f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5068f-105">Información para sincronizar un encabezado de mensaje durante el estado [del encabezado del mensaje de descarga.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="5068f-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5068f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="5068f-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="5068f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5068f-107">Members</span></span>

 <span data-ttu-id="5068f-108">_oemmsg_</span><span class="sxs-lookup"><span data-stu-id="5068f-108">_pupmsg_</span></span>
  
- <span data-ttu-id="5068f-109">[salida] Información del encabezado del mensaje actual en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="5068f-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="5068f-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="5068f-110">_feidPar_</span></span>
  
- <span data-ttu-id="5068f-111">[salida] Identificador de entrada de la carpeta principal del elemento de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5068f-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="5068f-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="5068f-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="5068f-113">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="5068f-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="5068f-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5068f-114">_ulFlags_</span></span>
  
- <span data-ttu-id="5068f-115">[entrada] Marcas para modificar el comportamiento:</span><span class="sxs-lookup"><span data-stu-id="5068f-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="5068f-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5068f-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="5068f-117">[entrada] El elemento completo reside en el mismo almacén local que el elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="5068f-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="5068f-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="5068f-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="5068f-119">[entrada] Optimizar las operaciones de copia internas.</span><span class="sxs-lookup"><span data-stu-id="5068f-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="5068f-120">Esto puede provocar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="5068f-120">This might cause data loss.</span></span> <span data-ttu-id="5068f-121">**HSF_LOCAL** se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="5068f-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="5068f-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="5068f-122">HSF_OK</span></span>
    
  - <span data-ttu-id="5068f-123">[entrada] La sincronización de encabezados se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5068f-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="5068f-124">El cliente lo establece después de descargar la información del servidor.</span><span class="sxs-lookup"><span data-stu-id="5068f-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="5068f-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="5068f-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="5068f-126">[entrada] El elemento de mensaje completo, incluido el encabezado del mensaje descargado del servidor.</span><span class="sxs-lookup"><span data-stu-id="5068f-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="5068f-127">Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="5068f-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5068f-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5068f-128">See also</span></span>



[<span data-ttu-id="5068f-129">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="5068f-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5068f-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="5068f-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5068f-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5068f-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5068f-132">FEID</span><span class="sxs-lookup"><span data-stu-id="5068f-132">FEID</span></span>](feid.md)

