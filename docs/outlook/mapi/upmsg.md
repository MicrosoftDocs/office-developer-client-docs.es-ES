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
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820947"
---
# <a name="upmsg"></a><span data-ttu-id="bcf84-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="bcf84-103">UPMSG</span></span>

<span data-ttu-id="bcf84-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bcf84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bcf84-105">Información para cargar un elemento de Outlook durante la [carga de estado del mensaje](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="bcf84-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bcf84-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="bcf84-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="bcf84-107">Members</span><span class="sxs-lookup"><span data-stu-id="bcf84-107">Members</span></span>

 <span data-ttu-id="bcf84-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bcf84-108">_ulFlags_</span></span>
  
> <span data-ttu-id="bcf84-109">[out] o [in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="bcf84-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="bcf84-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="bcf84-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="bcf84-111">[out] Elemento está asociado.</span><span class="sxs-lookup"><span data-stu-id="bcf84-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="bcf84-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="bcf84-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="bcf84-113">[out] Nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="bcf84-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="bcf84-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="bcf84-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="bcf84-115">[out] Elemento se ha movido aquí.</span><span class="sxs-lookup"><span data-stu-id="bcf84-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="bcf84-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="bcf84-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="bcf84-117">[out] Se modificaron las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="bcf84-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="bcf84-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="bcf84-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="bcf84-119">[out] Item es un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bcf84-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="bcf84-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="bcf84-120">UPM_OK</span></span>
    
    - <span data-ttu-id="bcf84-121">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="bcf84-121">[in] Upload was successful.</span></span> <span data-ttu-id="bcf84-122">El cliente establece esto después de cargar información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bcf84-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="bcf84-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="bcf84-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="bcf84-124">[entrada] Elemento se ha movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcf84-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="bcf84-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="bcf84-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="bcf84-126">[entrada] Confirmar ahora el estado de carga.</span><span class="sxs-lookup"><span data-stu-id="bcf84-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="bcf84-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="bcf84-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="bcf84-128">[entrada] Eliminar elemento ahora.</span><span class="sxs-lookup"><span data-stu-id="bcf84-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="bcf84-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="bcf84-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="bcf84-130">[entrada] Guarde los cambios en el elemento.</span><span class="sxs-lookup"><span data-stu-id="bcf84-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="bcf84-131">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="bcf84-131">_pmsg_</span></span>
  
> <span data-ttu-id="bcf84-132">[out] Objeto de elemento abierto.</span><span class="sxs-lookup"><span data-stu-id="bcf84-132">[out] Open item object.</span></span> <span data-ttu-id="bcf84-133">Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="bcf84-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="bcf84-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="bcf84-134">_meid_</span></span>
  
> <span data-ttu-id="bcf84-135">[out] Identificador de entrada del elemento.</span><span class="sxs-lookup"><span data-stu-id="bcf84-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="bcf84-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="bcf84-136">_binReserved1_</span></span>
  
> <span data-ttu-id="bcf84-137">[entrada] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="bcf84-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="bcf84-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="bcf84-138">_binReserved2_</span></span>
  
> <span data-ttu-id="bcf84-139">[entrada] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="bcf84-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="bcf84-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="bcf84-140">_feid_</span></span>
  
> <span data-ttu-id="bcf84-141">[out] Identificador de entrada de la carpeta de origen, si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="bcf84-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="bcf84-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="bcf84-142">_binChg_</span></span>
  
> <span data-ttu-id="bcf84-143">[out] Cambiar la clave del elemento de destino, si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="bcf84-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="bcf84-144">Vea mapidefs.h para la definición de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="bcf84-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="bcf84-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="bcf84-145">_binPcl_</span></span>
  
> <span data-ttu-id="bcf84-146">[out] Cambiar la lista del elemento de destino, si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="bcf84-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="bcf84-147">Vea mapidefs.h para la definición de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="bcf84-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="bcf84-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="bcf84-148">_skeySrc_</span></span>
  
> <span data-ttu-id="bcf84-149">[out] Clave de origen del elemento de origen, si el elemento se ha movido.</span><span class="sxs-lookup"><span data-stu-id="bcf84-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcf84-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcf84-150">See also</span></span>

- [<span data-ttu-id="bcf84-151">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="bcf84-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="bcf84-152">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="bcf84-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="bcf84-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf84-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="bcf84-154">FEID</span><span class="sxs-lookup"><span data-stu-id="bcf84-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="bcf84-155">MEID</span><span class="sxs-lookup"><span data-stu-id="bcf84-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="bcf84-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="bcf84-156">SKEY</span></span>](skey.md)

