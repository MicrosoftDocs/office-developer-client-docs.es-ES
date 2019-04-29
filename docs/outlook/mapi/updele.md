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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424885"
---
# <a name="updele"></a><span data-ttu-id="32eb7-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="32eb7-103">UPDELE</span></span>

<span data-ttu-id="32eb7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32eb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32eb7-105">Información extendida para los elementos que se han eliminado en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="32eb7-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="32eb7-106">Esta información se usa durante el [Estado de eliminación de carga](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="32eb7-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="32eb7-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="32eb7-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="32eb7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="32eb7-108">Members</span></span>

<span data-ttu-id="32eb7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32eb7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="32eb7-110">[salida]/[in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="32eb7-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="32eb7-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="32eb7-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="32eb7-112">contempla El elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="32eb7-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="32eb7-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="32eb7-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="32eb7-114">contempla Se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="32eb7-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="32eb7-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="32eb7-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="32eb7-116">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="32eb7-116">[in] Upload was successful.</span></span> <span data-ttu-id="32eb7-117">El cliente lo establece después de cargar la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="32eb7-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="32eb7-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="32eb7-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="32eb7-119">a El elemento se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="32eb7-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="32eb7-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="32eb7-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="32eb7-121">a Marcar el elemento de origen como modificado.</span><span class="sxs-lookup"><span data-stu-id="32eb7-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="32eb7-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="32eb7-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="32eb7-123">a Confirmar el estado de carga ahora (entrada 0).</span><span class="sxs-lookup"><span data-stu-id="32eb7-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="32eb7-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="32eb7-124">_skey_</span></span>
  
> <span data-ttu-id="32eb7-125">contempla Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="32eb7-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="32eb7-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="32eb7-126">_dwReserved_</span></span>
  
> <span data-ttu-id="32eb7-127">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="32eb7-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="32eb7-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="32eb7-128">_binChg_</span></span>
  
> <span data-ttu-id="32eb7-129">contempla Cambiar la clave del elemento de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="32eb7-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="32eb7-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="32eb7-130">_binPcl_</span></span>
  
> <span data-ttu-id="32eb7-131">contempla Cambia la lista de elementos de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="32eb7-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="32eb7-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="32eb7-132">_skeyDst_</span></span>
  
> <span data-ttu-id="32eb7-133">contempla Clave de origen del elemento de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="32eb7-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="32eb7-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="32eb7-134">_pupmov_</span></span>
  
> <span data-ttu-id="32eb7-135">contempla Información de la carpeta de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="32eb7-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32eb7-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="32eb7-136">See also</span></span>

- [<span data-ttu-id="32eb7-137">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="32eb7-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="32eb7-138">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="32eb7-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="32eb7-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="32eb7-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="32eb7-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="32eb7-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="32eb7-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="32eb7-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="32eb7-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="32eb7-142">UPMOV</span></span>](upmov.md)

