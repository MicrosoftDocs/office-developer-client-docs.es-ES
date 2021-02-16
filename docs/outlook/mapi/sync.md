---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433811"
---
# <a name="sync"></a><span data-ttu-id="9efa3-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="9efa3-103">SYNC</span></span>

  
  
<span data-ttu-id="9efa3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9efa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9efa3-105">Información para iniciar la sincronización entre un almacén local y un servidor.</span><span class="sxs-lookup"><span data-stu-id="9efa3-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="9efa3-106">Esta información se usa durante el [estado de sincronización.](synchronize-state.md)</span><span class="sxs-lookup"><span data-stu-id="9efa3-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9efa3-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9efa3-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="9efa3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9efa3-108">Members</span></span>

 <span data-ttu-id="9efa3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9efa3-109">_ulFlags_</span></span>
  
- <span data-ttu-id="9efa3-110">[out]/[in] Máscara de bits de las siguientes marcas que modifica el comportamiento durante la sincronización:</span><span class="sxs-lookup"><span data-stu-id="9efa3-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="9efa3-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9efa3-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9efa3-112">[entrada] El cliente solo realizará la carga.</span><span class="sxs-lookup"><span data-stu-id="9efa3-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="9efa3-113">Outlook solo devuelve carpetas modificadas localmente.</span><span class="sxs-lookup"><span data-stu-id="9efa3-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="9efa3-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9efa3-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9efa3-115">[entrada] El cliente solo realizará la descarga.</span><span class="sxs-lookup"><span data-stu-id="9efa3-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="9efa3-116">Outlook no debe borrar los bits de carga de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="9efa3-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="9efa3-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9efa3-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="9efa3-118">[entrada] El cliente sincronizará un conjunto especificado de carpetas con los identificadores de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="9efa3-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="9efa3-119">Esta marca se puede combinar con la **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY** marca.</span><span class="sxs-lookup"><span data-stu-id="9efa3-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="9efa3-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="9efa3-120">UPS_OK</span></span>
    
  - <span data-ttu-id="9efa3-121">[salida] La sincronización se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9efa3-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="9efa3-122">El cliente establece esto después de cargar o de completar una sincronización completa.</span><span class="sxs-lookup"><span data-stu-id="9efa3-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="9efa3-123">Aunque el cliente puede cargar o sincronizar completamente (cargar y descargar) carpetas y elementos con la API de replicación, el cliente especifica *ulFlags* con una sola dirección de la replicación a la vez, ya sea la marca **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="9efa3-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="9efa3-124">En el caso de una sincronización completa, el cliente primero realiza una carga con la marca **UPS_UPLOAD_ONLY** y, a continuación, una descarga con la **marca UPS_DNLOAD_ONLY** usuario.</span><span class="sxs-lookup"><span data-stu-id="9efa3-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="9efa3-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="9efa3-125">_pwzPath_</span></span>
  
- <span data-ttu-id="9efa3-126">[salida] Ruta de acceso al almacén local.</span><span class="sxs-lookup"><span data-stu-id="9efa3-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="9efa3-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="9efa3-127">_Reserved1_</span></span>
  
- <span data-ttu-id="9efa3-128">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="9efa3-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9efa3-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="9efa3-129">_Reserved2_</span></span>
  
- <span data-ttu-id="9efa3-130">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="9efa3-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9efa3-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="9efa3-131">*pel*</span></span> 
  
- <span data-ttu-id="9efa3-132">[entrada] Esta es la lista de identificadores de entrada de las carpetas que se sincronizarán **si UPS_THESE_FOLDERS** se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="9efa3-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9efa3-133">Vea mapidefs.h para obtener la definición de tipo **de LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="9efa3-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="9efa3-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="9efa3-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="9efa3-135">[entrada] Se trata de una matriz de opciones de carpeta para las carpetas  *correspondientes*  en pel **si UPS_THESE_FOLDERS** se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="9efa3-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9efa3-136">Estas opciones de carpeta se usan al cargar cada una de las carpetas enumeradas en *pel* durante el estado [de carga de la carpeta.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="9efa3-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="9efa3-137">Para obtener más información acerca de las opciones de carpeta, **[vea UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="9efa3-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9efa3-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9efa3-138">See also</span></span>



[<span data-ttu-id="9efa3-139">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="9efa3-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9efa3-140">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="9efa3-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9efa3-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9efa3-141">MAPI Constants</span></span>](mapi-constants.md)

