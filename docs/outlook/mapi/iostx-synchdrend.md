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
description: 'Última modificación: 3 de julio de 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332189"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="6b913-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="6b913-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="6b913-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b913-105">Termina la sincronización de un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b913-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="6b913-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b913-106">Parameters</span></span>

 <span data-ttu-id="6b913-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="6b913-107">_pprog_</span></span>
  
> <span data-ttu-id="6b913-108">a Interfaz **[método imapiprogress](imapiprogressiunknown.md)** para la sincronización de mensajes movidos o copiados.</span><span class="sxs-lookup"><span data-stu-id="6b913-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="6b913-109">Consulte mapidefs. h para obtener la definición de tipo de **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="6b913-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b913-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b913-110">Remarks</span></span>

<span data-ttu-id="6b913-111">Cuando **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, el almacén local escribe el [Estado del encabezado del mensaje de descarga](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="6b913-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="6b913-112">El cliente descarga un elemento de mensaje completo (como *pmsgFull* en **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="6b913-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="6b913-113">Si se realiza correctamente, el cliente también establece *ulFlags* en **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="6b913-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="6b913-114">Tras **IOSTX:: SyncHdrEnd**, Outlook comprueba el resultado en **HDRSYNC** y usa *Pprog* y la información de **HDRSYNC** para actualizar el encabezado del mensaje local.</span><span class="sxs-lookup"><span data-stu-id="6b913-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="6b913-115">El almacén local vuelve al estado en que se encontraba antes de la anterior **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="6b913-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b913-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b913-116">See also</span></span>



[<span data-ttu-id="6b913-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6b913-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="6b913-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="6b913-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="6b913-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="6b913-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="6b913-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="6b913-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="6b913-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="6b913-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="6b913-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="6b913-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="6b913-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b913-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="6b913-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6b913-124">MAPI Constants</span></span>](mapi-constants.md)

