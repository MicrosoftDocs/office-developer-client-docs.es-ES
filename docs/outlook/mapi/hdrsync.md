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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342787"
---
# <a name="hdrsync"></a><span data-ttu-id="2c381-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="2c381-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="2c381-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c381-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c381-105">Información para sincronizar un encabezado de mensaje durante el [Estado del encabezado del mensaje de descarga](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="2c381-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c381-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2c381-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="2c381-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c381-107">Members</span></span>

 <span data-ttu-id="2c381-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="2c381-108">_pupmsg_</span></span>
  
- <span data-ttu-id="2c381-109">contempla Información del encabezado del mensaje actual en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="2c381-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="2c381-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="2c381-110">_feidPar_</span></span>
  
- <span data-ttu-id="2c381-111">contempla IDENTIFICADOR de entrada de la carpeta principal del elemento de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2c381-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="2c381-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="2c381-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="2c381-113">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="2c381-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="2c381-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c381-114">_ulFlags_</span></span>
  
- <span data-ttu-id="2c381-115">a Marcas para modificar el comportamiento:</span><span class="sxs-lookup"><span data-stu-id="2c381-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="2c381-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2c381-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="2c381-117">a Elemento completo reside en el mismo almacén local que el elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2c381-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="2c381-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="2c381-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="2c381-119">a Optimizar las operaciones de copia internas.</span><span class="sxs-lookup"><span data-stu-id="2c381-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="2c381-120">Esto puede provocar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="2c381-120">This might cause data loss.</span></span> <span data-ttu-id="2c381-121">Se debe establecer **HSF_LOCAL** .</span><span class="sxs-lookup"><span data-stu-id="2c381-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="2c381-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="2c381-122">HSF_OK</span></span>
    
  - <span data-ttu-id="2c381-123">a La sincronización del encabezado se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c381-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="2c381-124">El cliente lo establece después de descargar la información del servidor.</span><span class="sxs-lookup"><span data-stu-id="2c381-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="2c381-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="2c381-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="2c381-126">a El elemento de mensaje completo, incluido el encabezado de mensaje descargado del servidor.</span><span class="sxs-lookup"><span data-stu-id="2c381-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="2c381-127">Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="2c381-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2c381-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c381-128">See also</span></span>



[<span data-ttu-id="2c381-129">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="2c381-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2c381-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="2c381-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2c381-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c381-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2c381-132">FEID</span><span class="sxs-lookup"><span data-stu-id="2c381-132">FEID</span></span>](feid.md)

