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
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429113"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="5ea09-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="5ea09-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="5ea09-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ea09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ea09-105">Actualiza el estado en el cuadro de diálogo De envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="5ea09-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="5ea09-106">El proveedor de almacenamiento llama periódicamente a esta función.</span><span class="sxs-lookup"><span data-stu-id="5ea09-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="5ea09-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea09-107">Parameters</span></span>

 <span data-ttu-id="5ea09-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="5ea09-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="5ea09-109">Puntero a una cadena que muestra el paso de progreso actual.</span><span class="sxs-lookup"><span data-stu-id="5ea09-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="5ea09-110">Puede ser NULL para actualizar el progreso.</span><span class="sxs-lookup"><span data-stu-id="5ea09-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="5ea09-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="5ea09-111">**ulIndex**</span></span>
  
> <span data-ttu-id="5ea09-112">Posición actual en curso.</span><span class="sxs-lookup"><span data-stu-id="5ea09-112">The current position in progress.</span></span>
    
 <span data-ttu-id="5ea09-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="5ea09-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="5ea09-114">Índice que indica el progreso completo.</span><span class="sxs-lookup"><span data-stu-id="5ea09-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ea09-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea09-115">Return value</span></span>

<span data-ttu-id="5ea09-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ea09-116">S_OK</span></span> 
  
> <span data-ttu-id="5ea09-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="5ea09-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ea09-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ea09-118">See also</span></span>



[<span data-ttu-id="5ea09-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ea09-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

