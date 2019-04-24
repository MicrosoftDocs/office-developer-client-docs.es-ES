---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315088"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="9ac94-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="9ac94-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="9ac94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ac94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ac94-105">Inicia una sesión de sincronización y obtiene la interfaz **[IOSTX](iostxiunknown.md)** asociada.</span><span class="sxs-lookup"><span data-stu-id="9ac94-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="9ac94-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9ac94-106">Parameters</span></span>

 <span data-ttu-id="9ac94-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="9ac94-107">_ppostx_</span></span>
  
>  <span data-ttu-id="9ac94-108">contempla Puntero a la interfaz **IOSTX** que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="9ac94-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9ac94-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ac94-109">Remarks</span></span>

<span data-ttu-id="9ac94-110">El autor de la llamada debe asegurarse de que la misma carpeta no esté sincronizada al mismo tiempo en más de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="9ac94-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ac94-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ac94-111">See also</span></span>



[<span data-ttu-id="9ac94-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="9ac94-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="9ac94-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9ac94-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

