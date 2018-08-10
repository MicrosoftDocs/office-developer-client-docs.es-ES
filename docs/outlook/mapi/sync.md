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
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820821"
---
# <a name="sync"></a><span data-ttu-id="53697-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="53697-103">SYNC</span></span>

  
  
<span data-ttu-id="53697-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53697-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53697-105">Información para iniciar la sincronización entre un almacén local y un servidor.</span><span class="sxs-lookup"><span data-stu-id="53697-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="53697-106">Esta información se usa durante la [sincronización de estado](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="53697-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="53697-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="53697-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="53697-108">Members</span><span class="sxs-lookup"><span data-stu-id="53697-108">Members</span></span>

 <span data-ttu-id="53697-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53697-109">_ulFlags_</span></span>
  
- <span data-ttu-id="53697-110">[out] o [in] una máscara de bits de los siguientes indicadores que modifica el comportamiento durante la sincronización:</span><span class="sxs-lookup"><span data-stu-id="53697-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="53697-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="53697-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="53697-112">[entrada] El cliente llevará a cabo solo carga.</span><span class="sxs-lookup"><span data-stu-id="53697-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="53697-113">Outlook sólo devuelve las carpetas localmente modificadas.</span><span class="sxs-lookup"><span data-stu-id="53697-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="53697-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="53697-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="53697-115">[entrada] El cliente llevará a cabo sólo descarga.</span><span class="sxs-lookup"><span data-stu-id="53697-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="53697-116">Outlook no debe borrar bits de carga para las carpetas.</span><span class="sxs-lookup"><span data-stu-id="53697-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="53697-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="53697-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="53697-118">[entrada] El cliente va a sincronizar un conjunto especificado de carpetas con los identificadores de entrada proporcionado.</span><span class="sxs-lookup"><span data-stu-id="53697-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="53697-119">Este indicador se puede combinar con marca de la **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="53697-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="53697-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="53697-120">UPS_OK</span></span>
    
  - <span data-ttu-id="53697-121">[out] Sincronización realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="53697-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="53697-122">El cliente establece esto después de cargar o se complete una sincronización completa.</span><span class="sxs-lookup"><span data-stu-id="53697-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="53697-123">Aunque el cliente puede cargar o totalmente sincronizar (cargar, a continuación, descargue) carpetas y elementos con la API de replicación, el cliente especifica *ulFlags* con una única dirección de la replicación en un momento: el **UPS_UPLOAD_ONLY** o Marca **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="53697-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="53697-124">En el caso de una sincronización completa, el cliente realiza primero una carga con el indicador **UPS_UPLOAD_ONLY** y, a continuación, una descarga con la marca **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="53697-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="53697-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="53697-125">_pwzPath_</span></span>
  
- <span data-ttu-id="53697-126">[out] Ruta de acceso en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="53697-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="53697-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="53697-127">_Reserved1_</span></span>
  
- <span data-ttu-id="53697-128">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="53697-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="53697-129">_Reservado2_</span><span class="sxs-lookup"><span data-stu-id="53697-129">_Reserved2_</span></span>
  
- <span data-ttu-id="53697-130">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="53697-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="53697-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="53697-131">*pel*</span></span> 
  
- <span data-ttu-id="53697-132">[entrada] Ésta es la lista de identificadores de las carpetas para sincronizar si se ha establecido **UPS_THESE_FOLDERS** de entrada.</span><span class="sxs-lookup"><span data-stu-id="53697-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="53697-133">Vea mapidefs.h para la definición de tipo de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="53697-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="53697-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="53697-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="53697-135">[entrada] Esto es una matriz de las opciones de carpeta para carpetas correspondientes en *pel* si se ha establecido **UPS_THESE_FOLDERS** .</span><span class="sxs-lookup"><span data-stu-id="53697-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="53697-136">Estas opciones de carpeta se usan cuando se carga cada una de las carpetas que aparecen en *pel* durante la [carga de estado de la carpeta](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="53697-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="53697-137">Para obtener más información acerca de las opciones de carpeta, consulte **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="53697-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="53697-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="53697-138">See also</span></span>



[<span data-ttu-id="53697-139">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="53697-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="53697-140">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="53697-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="53697-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="53697-141">MAPI Constants</span></span>](mapi-constants.md)

