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
ms.openlocfilehash: 2d05592d1fdcdcd53c8b7879f9cdcd432df1a3f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579469"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="86db8-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="86db8-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="86db8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86db8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86db8-105">Inicia la sincronización para un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="86db8-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="86db8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86db8-106">Parameters</span></span>

 <span data-ttu-id="86db8-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="86db8-107">_cbeid_</span></span>
  
> <span data-ttu-id="86db8-108">[entrada] El número de bytes en el identificador de entrada para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="86db8-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="86db8-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="86db8-109">_lpeid_</span></span>
  
> <span data-ttu-id="86db8-110">[entrada] El identificador de entrada para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="86db8-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="86db8-111">_PPV_</span><span class="sxs-lookup"><span data-stu-id="86db8-111">_ppv_</span></span>
  
>  <span data-ttu-id="86db8-112">[en] / [salida] puntero a la estructura **[HDRSYNC](hdrsync.md)** para el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="86db8-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86db8-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86db8-113">Remarks</span></span>

<span data-ttu-id="86db8-114">Una vez **IOSTX::SyncHdrBeg**, local almacenar transiciones para el [estado del encabezado de mensaje de descarga](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="86db8-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="86db8-115">Outlook inicializa para el cliente de la estructura **HDRSYNC** con la representación del encabezado del mensaje en el almacén y la carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="86db8-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="86db8-116">El cliente, a continuación, debe descargar un elemento de mensaje completa (como *pmsgFull* en **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="86db8-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="86db8-117">Si se ha realizado correctamente, el cliente también establece *ulFlags* de **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="86db8-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="86db8-118">Una vez **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook comprueba el resultado en **HDRSYNC** y utiliza la información de **HDRSYNC** para actualizar el encabezado del mensaje local.</span><span class="sxs-lookup"><span data-stu-id="86db8-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86db8-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86db8-119">See also</span></span>



[<span data-ttu-id="86db8-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="86db8-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="86db8-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="86db8-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="86db8-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="86db8-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="86db8-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="86db8-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="86db8-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="86db8-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="86db8-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="86db8-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="86db8-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86db8-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="86db8-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="86db8-127">MAPI Constants</span></span>](mapi-constants.md)

