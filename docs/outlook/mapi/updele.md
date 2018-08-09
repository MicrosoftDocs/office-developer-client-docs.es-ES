---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820926"
---
# <a name="updele"></a><span data-ttu-id="e1700-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="e1700-103">UPDELE</span></span>

<span data-ttu-id="e1700-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1700-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1700-105">Información extendida para los elementos que se han eliminado en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="e1700-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="e1700-106">Esta información se usa durante la [carga Eliminar estado](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="e1700-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1700-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e1700-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="e1700-108">Members</span><span class="sxs-lookup"><span data-stu-id="e1700-108">Members</span></span>

<span data-ttu-id="e1700-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1700-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e1700-110">[out] o [in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="e1700-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="e1700-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="e1700-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="e1700-112">[out] Elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="e1700-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="e1700-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="e1700-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="e1700-114">[out] Elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e1700-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="e1700-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="e1700-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="e1700-116">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="e1700-116">[in] Upload was successful.</span></span> <span data-ttu-id="e1700-117">El cliente establece esto después de cargar información al servidor.</span><span class="sxs-lookup"><span data-stu-id="e1700-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="e1700-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="e1700-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="e1700-119">[entrada] Elemento se ha movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1700-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="e1700-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="e1700-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="e1700-121">[entrada] Elemento de origen de marcar como modificado.</span><span class="sxs-lookup"><span data-stu-id="e1700-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="e1700-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e1700-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="e1700-123">[entrada] Confirmar el estado de carga ahora (entrada de 0).</span><span class="sxs-lookup"><span data-stu-id="e1700-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="e1700-124">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="e1700-124">_skey_</span></span>
  
> <span data-ttu-id="e1700-125">[out] Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="e1700-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="e1700-126">_dwReservado_</span><span class="sxs-lookup"><span data-stu-id="e1700-126">_dwReserved_</span></span>
  
> <span data-ttu-id="e1700-127">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="e1700-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="e1700-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="e1700-128">_binChg_</span></span>
  
> <span data-ttu-id="e1700-129">[out] Cambiar la clave del elemento de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e1700-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e1700-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="e1700-130">_binPcl_</span></span>
  
> <span data-ttu-id="e1700-131">[out] Cambiar la lista de elemento de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e1700-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e1700-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="e1700-132">_skeyDst_</span></span>
  
> <span data-ttu-id="e1700-133">[out] Clave de origen del elemento de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e1700-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e1700-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="e1700-134">_pupmov_</span></span>
  
> <span data-ttu-id="e1700-135">[out] Información de la carpeta de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e1700-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1700-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1700-136">See also</span></span>

- [<span data-ttu-id="e1700-137">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="e1700-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="e1700-138">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="e1700-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e1700-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e1700-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e1700-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="e1700-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="e1700-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="e1700-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="e1700-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="e1700-142">UPMOV</span></span>](upmov.md)

