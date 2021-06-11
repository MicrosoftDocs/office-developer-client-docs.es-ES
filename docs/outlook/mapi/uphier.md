---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414924"
---
# <a name="uphier"></a><span data-ttu-id="0ab07-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="0ab07-103">UPHIER</span></span>
 
<span data-ttu-id="0ab07-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ab07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ab07-105">Información para sincronizar una jerarquía de carpetas durante el [estado de jerarquía de carga](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="0ab07-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ab07-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0ab07-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="0ab07-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ab07-107">Members</span></span>

<span data-ttu-id="0ab07-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ab07-108">_ulFlags_</span></span>
  
> <span data-ttu-id="0ab07-109">[in] Marca para modificar el comportamiento al sincronizar la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="0ab07-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="0ab07-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="0ab07-110">UPH_OK</span></span>
    
    - <span data-ttu-id="0ab07-111">[in] Upload se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ab07-111">[in] Upload was successful.</span></span> <span data-ttu-id="0ab07-112">El cliente establece esto después de cargar correctamente información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0ab07-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="0ab07-113">Al ver esta marca, Outlook borra la información de contabilidad interna que indicaba la jerarquía de carpetas necesaria para actualizarse.</span><span class="sxs-lookup"><span data-stu-id="0ab07-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="0ab07-114">El cliente pasa el HRESULT si la carga no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ab07-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="0ab07-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="0ab07-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="0ab07-116">[salida] Este miembro está reservado para Outlook uso interno y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="0ab07-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="0ab07-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="0ab07-117">_iEnt_</span></span>
  
> <span data-ttu-id="0ab07-118">[salida] Index para realizar un seguimiento de la sincronización del número de carpetas especificadas por  *cEnt*  .</span><span class="sxs-lookup"><span data-stu-id="0ab07-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="0ab07-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="0ab07-119">_cEnt_</span></span>
  
> <span data-ttu-id="0ab07-120">[salida] Número de carpetas que no están sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="0ab07-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ab07-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ab07-121">See also</span></span>

- [<span data-ttu-id="0ab07-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="0ab07-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="0ab07-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="0ab07-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="0ab07-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0ab07-124">MAPI Constants</span></span>](mapi-constants.md)

