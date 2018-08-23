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
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584677"
---
# <a name="synccont"></a><span data-ttu-id="c82ab-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="c82ab-103">SYNCCONT</span></span>

<span data-ttu-id="c82ab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c82ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c82ab-105">Información para sincronizar el contenido de las carpetas especificadas en un almacén local con el servidor durante la [sincronización de estado del contenido](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="c82ab-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="c82ab-106">Esto implica que acaba de cargar, o una sincronización completa que implican una carga y, a continuación, una descarga.</span><span class="sxs-lookup"><span data-stu-id="c82ab-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c82ab-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c82ab-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c82ab-108">Members</span><span class="sxs-lookup"><span data-stu-id="c82ab-108">Members</span></span>

<span data-ttu-id="c82ab-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c82ab-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c82ab-110">[entrada] Marcas para determinar el comportamiento adecuado durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="c82ab-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="c82ab-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="c82ab-111">UPC_OK</span></span>
    
  - <span data-ttu-id="c82ab-112">[entrada] Cargar o sincronización completa realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c82ab-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="c82ab-113">El cliente establece esto después de la sincronización de la información con el servidor.</span><span class="sxs-lookup"><span data-stu-id="c82ab-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="c82ab-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="c82ab-114">_iEnt_</span></span>
  
> <span data-ttu-id="c82ab-115">[out] Índice que se va a realizar un seguimiento de sincronizar el contenido en el número de las carpetas especificadas por _ciento_.</span><span class="sxs-lookup"><span data-stu-id="c82ab-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="c82ab-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="c82ab-116">_cEnt_</span></span>
  
> <span data-ttu-id="c82ab-117">[out] Número de carpetas que se replican.</span><span class="sxs-lookup"><span data-stu-id="c82ab-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="c82ab-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="c82ab-118">_pvReserved_</span></span>
  
> <span data-ttu-id="c82ab-119">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="c82ab-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c82ab-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="c82ab-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="c82ab-121">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="c82ab-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c82ab-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="c82ab-122">_psosReserved_</span></span>
  
> <span data-ttu-id="c82ab-123">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="c82ab-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c82ab-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c82ab-124">See also</span></span>

- [<span data-ttu-id="c82ab-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="c82ab-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="c82ab-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="c82ab-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="c82ab-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ab-127">MAPI Constants</span></span>](mapi-constants.md)

