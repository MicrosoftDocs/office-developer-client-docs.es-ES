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
# <a name="synccont"></a><span data-ttu-id="d9dc2-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="d9dc2-103">SYNCCONT</span></span>

<span data-ttu-id="d9dc2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9dc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9dc2-105">Información para sincronizar el contenido de las carpetas especificadas en un almacén local con el servidor durante el [Estado Synchronize Contents](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="d9dc2-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="d9dc2-106">Esto solo implica carga o una sincronización completa que implique una carga y, a continuación, una descarga.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9dc2-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d9dc2-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d9dc2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9dc2-108">Members</span></span>

<span data-ttu-id="d9dc2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d9dc2-110">a Marcas para determinar el comportamiento adecuado durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="d9dc2-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="d9dc2-111">UPC_OK</span></span>
    
  - <span data-ttu-id="d9dc2-112">a La carga o la sincronización completa se han realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="d9dc2-113">El cliente lo establece después de sincronizar la información con el servidor.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="d9dc2-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-114">_iEnt_</span></span>
  
> <span data-ttu-id="d9dc2-115">contempla Índice para realizar un seguimiento de la sincronización del contenido en el número de carpetas especificado en _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="d9dc2-116">_Ciento_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-116">_cEnt_</span></span>
  
> <span data-ttu-id="d9dc2-117">contempla Número de carpetas que se van a replicar.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="d9dc2-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-118">_pvReserved_</span></span>
  
> <span data-ttu-id="d9dc2-119">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d9dc2-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="d9dc2-121">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d9dc2-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="d9dc2-122">_psosReserved_</span></span>
  
> <span data-ttu-id="d9dc2-123">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d9dc2-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d9dc2-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="d9dc2-124">See also</span></span>

- [<span data-ttu-id="d9dc2-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="d9dc2-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d9dc2-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="d9dc2-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d9dc2-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d9dc2-127">MAPI Constants</span></span>](mapi-constants.md)

