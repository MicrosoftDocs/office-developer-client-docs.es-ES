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
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817557"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="34e82-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="34e82-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="34e82-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34e82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34e82-105">Proporciona información detallada que se muestra en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="34e82-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="34e82-106">Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="34e82-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="34e82-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34e82-107">Parameters</span></span>

 <span data-ttu-id="34e82-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="34e82-108">**hResult**</span></span>
  
> <span data-ttu-id="34e82-109">HRESULT del error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="34e82-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="34e82-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="34e82-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="34e82-111">Un puntero a la cadena asociada con el error que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="34e82-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34e82-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34e82-112">Return value</span></span>

<span data-ttu-id="34e82-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="34e82-113">S_OK</span></span> 
  
> <span data-ttu-id="34e82-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="34e82-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34e82-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="34e82-115">See also</span></span>



[<span data-ttu-id="34e82-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34e82-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

