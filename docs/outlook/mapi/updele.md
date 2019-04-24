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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360546"
---
# <a name="updele"></a><span data-ttu-id="f93cd-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="f93cd-103">UPDELE</span></span>

<span data-ttu-id="f93cd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f93cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f93cd-105">Información extendida para los elementos que se han eliminado en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="f93cd-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="f93cd-106">Esta información se usa durante el [Estado de eliminación de carga](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="f93cd-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f93cd-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f93cd-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="f93cd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f93cd-108">Members</span></span>

<span data-ttu-id="f93cd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f93cd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f93cd-110">[salida]/[in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="f93cd-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="f93cd-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="f93cd-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="f93cd-112">contempla El elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="f93cd-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="f93cd-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="f93cd-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="f93cd-114">contempla Se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="f93cd-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="f93cd-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="f93cd-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="f93cd-116">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f93cd-116">[in] Upload was successful.</span></span> <span data-ttu-id="f93cd-117">El cliente lo establece después de cargar la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f93cd-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="f93cd-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="f93cd-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="f93cd-119">a El elemento se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="f93cd-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="f93cd-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="f93cd-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="f93cd-121">a Marcar el elemento de origen como modificado.</span><span class="sxs-lookup"><span data-stu-id="f93cd-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="f93cd-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="f93cd-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="f93cd-123">a Confirmar el estado de carga ahora (entrada 0).</span><span class="sxs-lookup"><span data-stu-id="f93cd-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="f93cd-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="f93cd-124">_skey_</span></span>
  
> <span data-ttu-id="f93cd-125">contempla Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="f93cd-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="f93cd-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="f93cd-126">_dwReserved_</span></span>
  
> <span data-ttu-id="f93cd-127">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="f93cd-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="f93cd-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="f93cd-128">_binChg_</span></span>
  
> <span data-ttu-id="f93cd-129">contempla Cambiar la clave del elemento de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="f93cd-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="f93cd-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="f93cd-130">_binPcl_</span></span>
  
> <span data-ttu-id="f93cd-131">contempla Cambia la lista de elementos de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="f93cd-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="f93cd-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="f93cd-132">_skeyDst_</span></span>
  
> <span data-ttu-id="f93cd-133">contempla Clave de origen del elemento de destino si se ha movido el elemento.</span><span class="sxs-lookup"><span data-stu-id="f93cd-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="f93cd-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="f93cd-134">_pupmov_</span></span>
  
> <span data-ttu-id="f93cd-135">contempla Información de la carpeta de destino si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="f93cd-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f93cd-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f93cd-136">See also</span></span>

- [<span data-ttu-id="f93cd-137">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="f93cd-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="f93cd-138">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="f93cd-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="f93cd-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f93cd-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="f93cd-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="f93cd-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="f93cd-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="f93cd-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="f93cd-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="f93cd-142">UPMOV</span></span>](upmov.md)

