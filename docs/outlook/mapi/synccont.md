---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430409"
---
# <a name="synccont"></a><span data-ttu-id="5b45f-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="5b45f-103">SYNCCONT</span></span>

<span data-ttu-id="5b45f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b45f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b45f-105">Información para sincronizar el contenido de las carpetas especificadas en un almacén local con el servidor durante el [estado de sincronización del contenido.](synchronize-contents-state.md)</span><span class="sxs-lookup"><span data-stu-id="5b45f-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="5b45f-106">Esto implica simplemente la carga o una sincronización completa que implica una carga y, a continuación, una descarga.</span><span class="sxs-lookup"><span data-stu-id="5b45f-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5b45f-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="5b45f-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="5b45f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b45f-108">Members</span></span>

<span data-ttu-id="5b45f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b45f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b45f-110">[entrada] Marcas para determinar el comportamiento adecuado durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="5b45f-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="5b45f-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="5b45f-111">UPC_OK</span></span>
    
  - <span data-ttu-id="5b45f-112">[entrada] La carga o sincronización completa se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b45f-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="5b45f-113">El cliente establece esto después de sincronizar la información con el servidor.</span><span class="sxs-lookup"><span data-stu-id="5b45f-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="5b45f-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="5b45f-114">_iEnt_</span></span>
  
> <span data-ttu-id="5b45f-115">[salida] Índice para realizar un seguimiento de la sincronización del contenido en el número de carpetas especificadas por  _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="5b45f-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="5b45f-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="5b45f-116">_cEnt_</span></span>
  
> <span data-ttu-id="5b45f-117">[salida] Número de carpetas que se replicarán.</span><span class="sxs-lookup"><span data-stu-id="5b45f-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="5b45f-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="5b45f-118">_pvReserved_</span></span>
  
> <span data-ttu-id="5b45f-119">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="5b45f-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5b45f-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="5b45f-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="5b45f-121">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="5b45f-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5b45f-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="5b45f-122">_psosReserved_</span></span>
  
> <span data-ttu-id="5b45f-123">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="5b45f-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5b45f-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5b45f-124">See also</span></span>

- [<span data-ttu-id="5b45f-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="5b45f-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="5b45f-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="5b45f-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="5b45f-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b45f-127">MAPI Constants</span></span>](mapi-constants.md)

