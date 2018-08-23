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
ms.openlocfilehash: 5803441486f01883d08cd99048d8eae133cd3f14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592132"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="39158-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="39158-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="39158-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39158-105">Actualiza el estado en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="39158-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="39158-106">El proveedor de almacenamiento periódicamente llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="39158-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="39158-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39158-107">Parameters</span></span>

 <span data-ttu-id="39158-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="39158-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="39158-109">Un puntero a una cadena que muestra el paso de progreso actual.</span><span class="sxs-lookup"><span data-stu-id="39158-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="39158-110">Puede ser NULL para actualizar el progreso.</span><span class="sxs-lookup"><span data-stu-id="39158-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="39158-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="39158-111">**ulIndex**</span></span>
  
> <span data-ttu-id="39158-112">La posición actual en curso.</span><span class="sxs-lookup"><span data-stu-id="39158-112">The current position in progress.</span></span>
    
 <span data-ttu-id="39158-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="39158-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="39158-114">El índice que indica el progreso completado.</span><span class="sxs-lookup"><span data-stu-id="39158-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39158-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39158-115">Return value</span></span>

<span data-ttu-id="39158-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="39158-116">S_OK</span></span> 
  
> <span data-ttu-id="39158-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="39158-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39158-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="39158-118">See also</span></span>



[<span data-ttu-id="39158-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39158-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

