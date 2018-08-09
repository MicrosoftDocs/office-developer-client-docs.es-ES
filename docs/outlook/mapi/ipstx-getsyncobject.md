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
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817950"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="25f78-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="25f78-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="25f78-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25f78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25f78-105">Inicia una sesión de sincronización y obtiene la interfaz **[IOSTX](iostxiunknown.md)** asociada.</span><span class="sxs-lookup"><span data-stu-id="25f78-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="25f78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25f78-106">Parameters</span></span>

 <span data-ttu-id="25f78-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="25f78-107">_ppostx_</span></span>
  
>  <span data-ttu-id="25f78-108">[out] Puntero a la interfaz **IOSTX** para obtener.</span><span class="sxs-lookup"><span data-stu-id="25f78-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="25f78-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25f78-109">Remarks</span></span>

<span data-ttu-id="25f78-110">El llamador debe asegurarse de que la misma carpeta no se sincroniza al mismo tiempo en más de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="25f78-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25f78-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="25f78-111">See also</span></span>



[<span data-ttu-id="25f78-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="25f78-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="25f78-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="25f78-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

