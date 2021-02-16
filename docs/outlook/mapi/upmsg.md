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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427272"
---
# <a name="upmsg"></a><span data-ttu-id="190b8-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="190b8-103">UPMSG</span></span>

<span data-ttu-id="190b8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="190b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="190b8-105">Información para cargar un elemento de Outlook durante el estado [del mensaje de carga.](upload-message-state.md)</span><span class="sxs-lookup"><span data-stu-id="190b8-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="190b8-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="190b8-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="190b8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="190b8-107">Members</span></span>

 <span data-ttu-id="190b8-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="190b8-108">_ulFlags_</span></span>
  
> <span data-ttu-id="190b8-109">[out]/[in] Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="190b8-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="190b8-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="190b8-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="190b8-111">[salida] El elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="190b8-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="190b8-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="190b8-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="190b8-113">[salida] Nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="190b8-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="190b8-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="190b8-115">[salida] El elemento se movió aquí.</span><span class="sxs-lookup"><span data-stu-id="190b8-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="190b8-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="190b8-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="190b8-117">[salida] Se modificaron las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="190b8-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="190b8-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="190b8-119">[salida] El elemento es un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="190b8-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="190b8-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="190b8-120">UPM_OK</span></span>
    
    - <span data-ttu-id="190b8-121">[entrada] La carga se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="190b8-121">[in] Upload was successful.</span></span> <span data-ttu-id="190b8-122">El cliente establece esto después de cargar información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="190b8-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="190b8-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="190b8-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="190b8-124">[entrada] El elemento se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="190b8-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="190b8-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="190b8-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="190b8-126">[entrada] Confirma el estado de carga ahora.</span><span class="sxs-lookup"><span data-stu-id="190b8-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="190b8-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="190b8-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="190b8-128">[entrada] Eliminar elemento ahora.</span><span class="sxs-lookup"><span data-stu-id="190b8-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="190b8-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="190b8-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="190b8-130">[entrada] Guarde los cambios en el elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="190b8-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="190b8-131">_pmsg_</span></span>
  
> <span data-ttu-id="190b8-132">[salida] Abrir objeto de elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-132">[out] Open item object.</span></span> <span data-ttu-id="190b8-133">Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="190b8-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="190b8-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="190b8-134">_meid_</span></span>
  
> <span data-ttu-id="190b8-135">[salida] Identificador de entrada del elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="190b8-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="190b8-136">_binReserved1_</span></span>
  
> <span data-ttu-id="190b8-137">[entrada] Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="190b8-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="190b8-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="190b8-138">_binReserved2_</span></span>
  
> <span data-ttu-id="190b8-139">[entrada] Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="190b8-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="190b8-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="190b8-140">_feid_</span></span>
  
> <span data-ttu-id="190b8-141">[salida] Identificador de entrada de la carpeta de origen, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="190b8-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="190b8-142">_binChg_</span></span>
  
> <span data-ttu-id="190b8-143">[salida] Cambiar la clave del elemento de destino, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="190b8-144">Vea mapidefs.h para obtener la definición de tipo **de SBinary**.</span><span class="sxs-lookup"><span data-stu-id="190b8-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="190b8-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="190b8-145">_binPcl_</span></span>
  
> <span data-ttu-id="190b8-146">[salida] Cambiar la lista del elemento de destino, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="190b8-147">Vea mapidefs.h para obtener la definición de tipo **de SBinary**.</span><span class="sxs-lookup"><span data-stu-id="190b8-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="190b8-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="190b8-148">_skeySrc_</span></span>
  
> <span data-ttu-id="190b8-149">[salida] Clave de origen del elemento de origen, si se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="190b8-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="190b8-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="190b8-150">See also</span></span>

- [<span data-ttu-id="190b8-151">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="190b8-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="190b8-152">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="190b8-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="190b8-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="190b8-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="190b8-154">FEID</span><span class="sxs-lookup"><span data-stu-id="190b8-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="190b8-155">MEID</span><span class="sxs-lookup"><span data-stu-id="190b8-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="190b8-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="190b8-156">SKEY</span></span>](skey.md)

