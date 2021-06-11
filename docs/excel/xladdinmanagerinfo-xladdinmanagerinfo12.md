---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- función xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407798"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="e7023-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="e7023-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="e7023-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e7023-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e7023-106">Se llama Microsoft Excel cuando se invoca el Administrador de complementos por primera vez en una Excel sesión.</span><span class="sxs-lookup"><span data-stu-id="e7023-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="e7023-107">Esta función se usa para proporcionar al administrador de Add-In información sobre el complemento.</span><span class="sxs-lookup"><span data-stu-id="e7023-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="e7023-108">Excel 2007 y versiones posteriores llaman **a xlAddInManagerInfo12** con preferencia a **xlAddInManagerInfo** si se exporta mediante XLL.</span><span class="sxs-lookup"><span data-stu-id="e7023-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="e7023-109">La **función xlAddInManagerInfo12** debe funcionar del mismo modo que **xlAddInManagerInfo** para evitar diferencias específicas de versión en el comportamiento de XLL.</span><span class="sxs-lookup"><span data-stu-id="e7023-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="e7023-110">Excel espera que **xlAddInManagerInfo12** devuelva un tipo de datos **XLOPER12,** mientras **que xlAddInManagerInfo** debe devolver un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="e7023-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="e7023-111">Las versiones de Excel anteriores a Excel 2007 no llaman a la función **xlAddInManagerInfo12,** ya que no **admiten XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="e7023-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="e7023-112">Excel requiere un XLL para implementar y exportar ninguna de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="e7023-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="e7023-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="e7023-113">Parameters</span></span>

 <span data-ttu-id="e7023-114">_pxAction:_ Puntero a un **XLOPER/XLOPER12** numérico (**xltypeInt** o **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="e7023-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="e7023-115">La información que Excel está solicitando.</span><span class="sxs-lookup"><span data-stu-id="e7023-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e7023-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7023-116">Property value/Return value</span></span>

<span data-ttu-id="e7023-117">Si  _pxAction_ es o se puede coaccionar al número 1, la implementación de esta función debe devolver una cadena que contenga información sobre el complemento, normalmente su nombre y quizás un número de versión.</span><span class="sxs-lookup"><span data-stu-id="e7023-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="e7023-118">De lo contrario, debería devolver #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="e7023-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="e7023-119">Si no devuelve una cadena, Excel intenta convertir el valor devuelto en una cadena.</span><span class="sxs-lookup"><span data-stu-id="e7023-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7023-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7023-120">Remarks</span></span>

<span data-ttu-id="e7023-121">Si la cadena devuelta apunta al búfer asignado dinámicamente, debe asegurarse de que este búfer se libera finalmente.</span><span class="sxs-lookup"><span data-stu-id="e7023-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="e7023-122">Si la cadena se asignó Excel, debe hacerlo estableciendo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="e7023-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="e7023-123">Si la cadena se asignó mediante el DLL, debe establecer **xlbitDLLFree** y también debe implementar en [xlAutoFree](xlautofree-xlautofree12.md) (si devuelve un **XLOPER**) o **xlAutoFree12** (si devuelve un **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="e7023-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="e7023-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7023-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="e7023-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7023-125">See also</span></span>



[<span data-ttu-id="e7023-126">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="e7023-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

