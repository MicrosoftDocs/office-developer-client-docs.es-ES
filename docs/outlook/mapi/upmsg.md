---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338874"
---
# <a name="upmsg"></a><span data-ttu-id="96841-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="96841-103">UPMSG</span></span>

<span data-ttu-id="96841-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96841-105">Información para cargar un elemento de Outlook durante el [Estado de carga del mensaje](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="96841-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96841-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="96841-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="96841-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="96841-107">Members</span></span>

 <span data-ttu-id="96841-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="96841-108">_ulFlags_</span></span>
  
> <span data-ttu-id="96841-109">[salida]/[in] Flags para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="96841-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="96841-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="96841-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="96841-111">contempla El elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="96841-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="96841-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="96841-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="96841-113">contempla Nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="96841-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="96841-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="96841-115">contempla El elemento se movió aquí.</span><span class="sxs-lookup"><span data-stu-id="96841-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="96841-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="96841-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="96841-117">contempla Se modificaron las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="96841-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="96841-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="96841-119">contempla Item es un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="96841-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="96841-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="96841-120">UPM_OK</span></span>
    
    - <span data-ttu-id="96841-121">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="96841-121">[in] Upload was successful.</span></span> <span data-ttu-id="96841-122">El cliente lo establece después de cargar la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="96841-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="96841-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="96841-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="96841-124">a El elemento se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="96841-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="96841-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="96841-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="96841-126">a Confirmar el estado de carga ahora.</span><span class="sxs-lookup"><span data-stu-id="96841-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="96841-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="96841-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="96841-128">a Eliminar elemento ahora.</span><span class="sxs-lookup"><span data-stu-id="96841-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="96841-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="96841-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="96841-130">a Guarde los cambios realizados en el elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="96841-131">_PMSG_</span><span class="sxs-lookup"><span data-stu-id="96841-131">_pmsg_</span></span>
  
> <span data-ttu-id="96841-132">contempla Objeto de elemento abierto.</span><span class="sxs-lookup"><span data-stu-id="96841-132">[out] Open item object.</span></span> <span data-ttu-id="96841-133">Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="96841-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="96841-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="96841-134">_meid_</span></span>
  
> <span data-ttu-id="96841-135">contempla IDENTIFICADOR de entrada del elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="96841-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="96841-136">_binReserved1_</span></span>
  
> <span data-ttu-id="96841-137">a Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="96841-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="96841-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="96841-138">_binReserved2_</span></span>
  
> <span data-ttu-id="96841-139">a Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="96841-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="96841-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="96841-140">_feid_</span></span>
  
> <span data-ttu-id="96841-141">contempla IDENTIFICADOR de entrada de la carpeta de origen, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="96841-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="96841-142">_binChg_</span></span>
  
> <span data-ttu-id="96841-143">contempla Cambiar la clave del elemento de destino, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="96841-144">Consulte mapidefs. h para obtener la definición de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="96841-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="96841-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="96841-145">_binPcl_</span></span>
  
> <span data-ttu-id="96841-146">contempla Cambiar la lista del elemento de destino, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="96841-147">Consulte mapidefs. h para obtener la definición de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="96841-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="96841-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="96841-148">_skeySrc_</span></span>
  
> <span data-ttu-id="96841-149">contempla Clave de origen del elemento de origen, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="96841-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96841-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="96841-150">See also</span></span>

- [<span data-ttu-id="96841-151">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="96841-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="96841-152">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="96841-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="96841-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="96841-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="96841-154">FEID</span><span class="sxs-lookup"><span data-stu-id="96841-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="96841-155">MEID</span><span class="sxs-lookup"><span data-stu-id="96841-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="96841-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="96841-156">SKEY</span></span>](skey.md)

