---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591334"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="4c708-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="4c708-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="4c708-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c708-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c708-105">Finaliza la sincronización para un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c708-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="4c708-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c708-106">Parameters</span></span>

 <span data-ttu-id="4c708-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="4c708-107">_pprog_</span></span>
  
> <span data-ttu-id="4c708-108">[entrada] Interfaz **[IMAPIProgress](imapiprogressiunknown.md)** para la sincronización de mover o copia mensajes.</span><span class="sxs-lookup"><span data-stu-id="4c708-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="4c708-109">Vea mapidefs.h para la definición de tipo de **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="4c708-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4c708-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c708-110">Remarks</span></span>

<span data-ttu-id="4c708-111">Una vez **[IOSTX::SyncBeg](iostx-syncbeg.md)**, el almacén local entra en el [estado del encabezado de mensaje de descarga](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="4c708-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="4c708-112">El cliente descarga un elemento de mensaje completa (como *pmsgFull* en **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="4c708-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="4c708-113">Si esto se realiza correctamente, el cliente establece también *ulFlags* en **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="4c708-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="4c708-114">Una vez **IOSTX::SyncHdrEnd**, Outlook comprueba el resultado en **HDRSYNC** y usa *pprog* y la información en **HDRSYNC** para actualizar el encabezado del mensaje local.</span><span class="sxs-lookup"><span data-stu-id="4c708-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="4c708-115">El almacén local se devuelve al estado que tenía antes de la anterior **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="4c708-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c708-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4c708-116">See also</span></span>



[<span data-ttu-id="4c708-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4c708-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="4c708-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="4c708-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="4c708-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="4c708-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="4c708-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="4c708-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="4c708-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="4c708-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="4c708-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="4c708-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="4c708-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c708-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="4c708-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4c708-124">MAPI Constants</span></span>](mapi-constants.md)

