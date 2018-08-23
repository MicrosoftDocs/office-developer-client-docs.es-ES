---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594988"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="f1b15-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="f1b15-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="f1b15-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1b15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1b15-105">Proporciona información detallada que se muestra en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="f1b15-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="f1b15-106">Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="f1b15-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="f1b15-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1b15-107">Parameters</span></span>

 <span data-ttu-id="f1b15-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="f1b15-108">**hResult**</span></span>
  
> <span data-ttu-id="f1b15-109">HRESULT del error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="f1b15-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="f1b15-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="f1b15-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="f1b15-111">Un puntero a la cadena asociada con el error que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="f1b15-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1b15-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b15-112">Return value</span></span>

<span data-ttu-id="f1b15-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1b15-113">S_OK</span></span> 
  
> <span data-ttu-id="f1b15-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f1b15-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1b15-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f1b15-115">See also</span></span>



[<span data-ttu-id="f1b15-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1b15-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

