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
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432775"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="c89cb-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="c89cb-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="c89cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c89cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c89cb-105">Finaliza la sincronización de un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c89cb-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="c89cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c89cb-106">Parameters</span></span>

 <span data-ttu-id="c89cb-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="c89cb-107">_pprog_</span></span>
  
> <span data-ttu-id="c89cb-108">[entrada] **[Interfaz IMAPIProgress](imapiprogressiunknown.md)** para la sincronización de mensajes movidos o copiados.</span><span class="sxs-lookup"><span data-stu-id="c89cb-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="c89cb-109">Vea mapidefs.h para obtener la definición de tipo **de LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="c89cb-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c89cb-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c89cb-110">Remarks</span></span>

<span data-ttu-id="c89cb-111">En **[IOSTX::SyncBeg,](iostx-syncbeg.md)** el almacén local escribe el estado de encabezado [del mensaje de descarga.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="c89cb-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="c89cb-112">El cliente descarga un elemento de mensaje completo  *(como pmsgFull*  en **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="c89cb-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="c89cb-113">Si se realiza correctamente, el cliente también establece  *ulFlags*  en **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="c89cb-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="c89cb-114">En **IOSTX::SyncHdrEnd,** Outlook comprueba el resultado en **HDRSYNC** y usa  *pprero*  y la información de **HDRSYNC** para actualizar el encabezado del mensaje local.</span><span class="sxs-lookup"><span data-stu-id="c89cb-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="c89cb-115">El almacén local vuelve al estado en el que estaba antes del **[IOSTX::SyncHdrBeg anterior.](iostx-synchdrbeg.md)**</span><span class="sxs-lookup"><span data-stu-id="c89cb-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c89cb-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c89cb-116">See also</span></span>



[<span data-ttu-id="c89cb-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c89cb-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="c89cb-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="c89cb-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="c89cb-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="c89cb-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="c89cb-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="c89cb-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="c89cb-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="c89cb-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="c89cb-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="c89cb-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="c89cb-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c89cb-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="c89cb-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c89cb-124">MAPI Constants</span></span>](mapi-constants.md)

