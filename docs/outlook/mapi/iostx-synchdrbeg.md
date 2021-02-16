---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405096"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="abd3e-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="abd3e-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="abd3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abd3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abd3e-105">Inicia la sincronización de un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="abd3e-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="abd3e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abd3e-106">Parameters</span></span>

 <span data-ttu-id="abd3e-107">_cgnid_</span><span class="sxs-lookup"><span data-stu-id="abd3e-107">_cbeid_</span></span>
  
> <span data-ttu-id="abd3e-108">[entrada] El número de bytes del identificador de entrada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="abd3e-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="abd3e-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="abd3e-109">_lpeid_</span></span>
  
> <span data-ttu-id="abd3e-110">[entrada] Identificador de entrada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="abd3e-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="abd3e-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="abd3e-111">_ppv_</span></span>
  
>  <span data-ttu-id="abd3e-112">[entrada]/[salida] Puntero a la estructura **[HDRSYNC](hdrsync.md)** del encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="abd3e-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="abd3e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abd3e-113">Remarks</span></span>

<span data-ttu-id="abd3e-114">En **IOSTX::SyncHdrBeg,** el almacén local pasa al estado de encabezado [del mensaje de descarga.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="abd3e-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="abd3e-115">Outlook inicializa para el cliente la estructura **HDRSYNC** con la representación actual del encabezado del mensaje en el almacén y la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="abd3e-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="abd3e-116">A continuación, el cliente debe descargar un elemento de mensaje completo  *(como pmsgFull*  en **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="abd3e-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="abd3e-117">Si se ha realizado correctamente, el cliente también establece  *ulFlags*  en **HDRSYNC** **como HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="abd3e-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="abd3e-118">En **[IOSTX::SyncHdrEnd,](iostx-synchdrend.md)** Outlook comprueba el resultado en **HDRSYNC** y usa la información de **HDRSYNC** para actualizar el encabezado del mensaje local.</span><span class="sxs-lookup"><span data-stu-id="abd3e-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abd3e-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="abd3e-119">See also</span></span>



[<span data-ttu-id="abd3e-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="abd3e-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="abd3e-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="abd3e-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="abd3e-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="abd3e-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="abd3e-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="abd3e-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="abd3e-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="abd3e-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="abd3e-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="abd3e-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="abd3e-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="abd3e-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="abd3e-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="abd3e-127">MAPI Constants</span></span>](mapi-constants.md)

