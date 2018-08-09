---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815515"
---
# <a name="calludf"></a><span data-ttu-id="04098-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="04098-103">CallUDF</span></span>

<span data-ttu-id="04098-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="04098-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="04098-105">Llama a una función definida por el usuario en un entorno informático de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="04098-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="04098-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04098-106">Parameters</span></span>

<span data-ttu-id="04098-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="04098-107">_SessionId_</span></span>
  
> <span data-ttu-id="04098-108">El identificador de la sesión en el que se va a realizar la llamada.</span><span class="sxs-lookup"><span data-stu-id="04098-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="04098-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="04098-109">_XLLName_</span></span>
  
> <span data-ttu-id="04098-110">El nombre del XLL que contiene la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="04098-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="04098-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="04098-111">_UDFName_</span></span>
  
> <span data-ttu-id="04098-112">El nombre de la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="04098-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="04098-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="04098-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="04098-114">La función que el conector debe llamar cuando se completa la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="04098-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="04098-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="04098-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="04098-116">El identificador asincrónico utilizado por Excel y el conector para realizar un seguimiento de la llamada de función definida por el usuario pendiente.</span><span class="sxs-lookup"><span data-stu-id="04098-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="04098-117">El conector utiliza más adelante cuando finalice la llamada, cuando llama a Excel mediante el puntero de función se pasa en el argumento _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="04098-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="04098-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="04098-118">_ArgCount_</span></span>
  
> <span data-ttu-id="04098-119">El número de argumentos que se pasan a la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="04098-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="04098-120">El valor máximo permitido es de 255.</span><span class="sxs-lookup"><span data-stu-id="04098-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="04098-121">_Parámetro1_</span><span class="sxs-lookup"><span data-stu-id="04098-121">_Parameter1_</span></span>
  
> <span data-ttu-id="04098-122">Un valor que se pase a la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="04098-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="04098-123">Repita este argumento para cada parámetro indicado por _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="04098-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04098-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04098-124">Return value</span></span>

<span data-ttu-id="04098-125">**xlHpcRetSuccess** si la llamada UDF se inicia correctamente; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores, incluidos el tiempo de espera. Si la llamada devuelve cualquier código de error (nada excepto **xlHpcRetSuccess**), a continuación, Excel considera la llamada UDF al que se ha producido un error, invalida la _pxAsyncHandle_y no espera a que se produzca una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="04098-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04098-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04098-126">Remarks</span></span>

<span data-ttu-id="04098-127">Esta función se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="04098-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04098-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04098-128">See also</span></span>

- [<span data-ttu-id="04098-129">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="04098-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

