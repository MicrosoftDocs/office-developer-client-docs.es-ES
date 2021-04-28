---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062028"
---
# <a name="imapiinitmonitorisinitialized"></a><span data-ttu-id="ce354-103">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="ce354-103">IMAPIInitMonitor::IsInitialized</span></span>
  
<span data-ttu-id="ce354-104">**Se aplica a**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="ce354-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="ce354-105">Consulta MAPI para determinar si se inicializa actualmente en el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce354-105">Queries MAPI to determine if it currently initialized in the calling process.</span></span>

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a><span data-ttu-id="ce354-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce354-106">Parameters</span></span>
<span data-ttu-id="ce354-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ce354-107">None</span></span>

## <a name="return-value"></a><span data-ttu-id="ce354-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce354-108">Return value</span></span>
<span data-ttu-id="ce354-109">Un BOOL que indica el estado actual de inicialización MAPI, un valor de TRUE significa que MAPI se ha inicializado y está disponible para su uso, mientras que un valor de FALSE significa que MAPI no está inicializado y no está listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="ce354-109">A BOOL indicating the current state of MAPI initialization, a value of TRUE means MAPI has been initialized and is available for use, while a value of FALSE means MAPI is currenty uninitialized and is not ready be consumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce354-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce354-110">Remarks</span></span>
<span data-ttu-id="ce354-111">Esto se puede usar para determinar si MAPI está listo para usarse, por ejemplo, si la aplicación quería hacer algo solo si MAPI ya se ha inicializado, esto podría ser una comprobación útil en una tarea en segundo plano para evitar el costo de girar MAPI para el trabajo opcional.</span><span class="sxs-lookup"><span data-stu-id="ce354-111">This can be used to determine if MAPI is ready to be used, for example, if your application wanted to do something only if MAPI has already be initialized, this could be a useful check in a background task to prevent the cost of spinning up MAPI for optional work.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce354-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce354-112">See also</span></span>

[<span data-ttu-id="ce354-113">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="ce354-113">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="ce354-114">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="ce354-114">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
