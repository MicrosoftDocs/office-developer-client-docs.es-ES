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
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424934"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="a876a-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="a876a-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="a876a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a876a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a876a-105">Proporciona detalles que se muestran en el cuadro de diálogo de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="a876a-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="a876a-106">Si se detectan errores durante la sincronización, el proveedor del almacén llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="a876a-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="a876a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a876a-107">Parameters</span></span>

 <span data-ttu-id="a876a-108">**Valores**</span><span class="sxs-lookup"><span data-stu-id="a876a-108">**hResult**</span></span>
  
> <span data-ttu-id="a876a-109">HRESULT del error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="a876a-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="a876a-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="a876a-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="a876a-111">Un puntero a la cadena asociada con el error que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="a876a-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a876a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a876a-112">Return value</span></span>

<span data-ttu-id="a876a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a876a-113">S_OK</span></span> 
  
> <span data-ttu-id="a876a-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a876a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a876a-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="a876a-115">See also</span></span>



[<span data-ttu-id="a876a-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a876a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

