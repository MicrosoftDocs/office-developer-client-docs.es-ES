---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817559"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="9d0c8-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="9d0c8-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="9d0c8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d0c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d0c8-105">Actualiza el estado en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="9d0c8-106">El proveedor de almacenamiento periódicamente llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="9d0c8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d0c8-107">Parameters</span></span>

 <span data-ttu-id="9d0c8-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="9d0c8-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="9d0c8-109">Un puntero a una cadena que muestra el paso de progreso actual.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="9d0c8-110">Puede ser NULL para actualizar el progreso.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="9d0c8-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="9d0c8-111">**ulIndex**</span></span>
  
> <span data-ttu-id="9d0c8-112">La posición actual en curso.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-112">The current position in progress.</span></span>
    
 <span data-ttu-id="9d0c8-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="9d0c8-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="9d0c8-114">El índice que indica el progreso completado.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d0c8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d0c8-115">Return value</span></span>

<span data-ttu-id="9d0c8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d0c8-116">S_OK</span></span> 
  
> <span data-ttu-id="9d0c8-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d0c8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d0c8-118">See also</span></span>



[<span data-ttu-id="9d0c8-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d0c8-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

