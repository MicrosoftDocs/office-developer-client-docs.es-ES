---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304168"
---
# <a name="calludf"></a><span data-ttu-id="8af7d-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="8af7d-103">CallUDF</span></span>

<span data-ttu-id="8af7d-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8af7d-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8af7d-105">Llama a una función definida por el usuario en un entorno informático de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8af7d-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="8af7d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8af7d-106">Parameters</span></span>

<span data-ttu-id="8af7d-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="8af7d-107">_SessionId_</span></span>
  
> <span data-ttu-id="8af7d-108">IDENTIFICADOR de la sesión en la que se va a realizar la llamada.</span><span class="sxs-lookup"><span data-stu-id="8af7d-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="8af7d-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="8af7d-109">_XLLName_</span></span>
  
> <span data-ttu-id="8af7d-110">El nombre del XLL que contiene la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="8af7d-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="8af7d-111">_UDFName_</span></span>
  
> <span data-ttu-id="8af7d-112">Nombre de la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="8af7d-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="8af7d-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="8af7d-114">La función a la que debe llamar el conector cuando finaliza la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="8af7d-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="8af7d-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="8af7d-116">El identificador asincrónico usado por Excel y el conector para realizar un seguimiento de la llamada pendiente a la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="8af7d-117">El conector lo usa más adelante cuando finaliza la llamada, cuando vuelve a llamar a Excel con el puntero de función pasado en el argumento _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="8af7d-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="8af7d-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="8af7d-118">_ArgCount_</span></span>
  
> <span data-ttu-id="8af7d-119">Número de argumentos que se van a pasar a la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="8af7d-120">El valor máximo permitido es 255.</span><span class="sxs-lookup"><span data-stu-id="8af7d-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="8af7d-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="8af7d-121">_Parameter1_</span></span>
  
> <span data-ttu-id="8af7d-122">Valor que se va a pasar a la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af7d-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="8af7d-123">Repita este argumento para cada parámetro indicado por _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="8af7d-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8af7d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8af7d-124">Return value</span></span>

<span data-ttu-id="8af7d-125">**xlHpcRetSuccess** si la llamada a la UDF se inicia correctamente; **xlHpcRetInvalidSessionId** si el argumento _SessionID_ no es válido; **xlHpcRetCallFailed** en otros errores, incluido el tiempo de espera. Si la llamada devuelve un código de error (cualquier cosa excepto **xlHpcRetSuccess**), Excel considera que la llamada a UDF no ha podido realizarse, invalida el _pxAsyncHandle_y no espera que se produzca una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8af7d-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8af7d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8af7d-126">Remarks</span></span>

<span data-ttu-id="8af7d-127">Esta función se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8af7d-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8af7d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8af7d-128">See also</span></span>

- [<span data-ttu-id="8af7d-129">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="8af7d-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

