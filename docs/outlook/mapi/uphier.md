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
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592097"
---
# <a name="uphier"></a><span data-ttu-id="1e43b-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="1e43b-103">UPHIER</span></span>
 
<span data-ttu-id="1e43b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e43b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e43b-105">Información para la sincronización de una jerarquía de carpetas durante la [carga de estado de la jerarquía](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="1e43b-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1e43b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1e43b-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="1e43b-107">Members</span><span class="sxs-lookup"><span data-stu-id="1e43b-107">Members</span></span>

<span data-ttu-id="1e43b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e43b-108">_ulFlags_</span></span>
  
> <span data-ttu-id="1e43b-109">[entrada] Marcas para modificar el comportamiento cuando se sincroniza la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="1e43b-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="1e43b-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="1e43b-110">UPH_OK</span></span>
    
    - <span data-ttu-id="1e43b-111">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="1e43b-111">[in] Upload was successful.</span></span> <span data-ttu-id="1e43b-112">El cliente establece esto después de cargar correctamente la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1e43b-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="1e43b-113">Al ver esta marca, Outlook borra cualquier información de contabilidad interna que indica que la jerarquía de carpetas sea necesario actualizar.</span><span class="sxs-lookup"><span data-stu-id="1e43b-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="1e43b-114">El cliente pasa el HRESULT si la carga no se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1e43b-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="1e43b-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="1e43b-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="1e43b-116">[out] Este miembro está reservado para uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="1e43b-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="1e43b-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="1e43b-117">_iEnt_</span></span>
  
> <span data-ttu-id="1e43b-118">[out] Índice que se va a realizar un seguimiento de sincronizar el número de las carpetas especificadas por *ciento* .</span><span class="sxs-lookup"><span data-stu-id="1e43b-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="1e43b-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="1e43b-119">_cEnt_</span></span>
  
> <span data-ttu-id="1e43b-120">[out] Número de carpetas que no están sincronizados.</span><span class="sxs-lookup"><span data-stu-id="1e43b-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e43b-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1e43b-121">See also</span></span>

- [<span data-ttu-id="1e43b-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1e43b-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1e43b-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="1e43b-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1e43b-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1e43b-124">MAPI Constants</span></span>](mapi-constants.md)

