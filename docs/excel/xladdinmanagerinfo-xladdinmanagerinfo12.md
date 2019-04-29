---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- función xladdinmanagerinfo [Excel 2007]
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
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="7a97b-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="7a97b-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="7a97b-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7a97b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7a97b-106">Llamado por Microsoft Excel cuando se invoca el administrador de complementos por primera vez en una sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="7a97b-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="7a97b-107">Esta función se usa para proporcionar al administrador de complementos información sobre el complemento.</span><span class="sxs-lookup"><span data-stu-id="7a97b-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="7a97b-108">Excel 2007 y versiones posteriores llaman a **xlAddInManagerInfo12** en prioridad a **xlAddInManagerInfo** si se exportan por el XLL.</span><span class="sxs-lookup"><span data-stu-id="7a97b-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="7a97b-109">La función **xlAddInManagerInfo12** debe funcionar de la misma manera que **xlAddInManagerInfo** para evitar diferencias específicas de la versión en el comportamiento del XLL.</span><span class="sxs-lookup"><span data-stu-id="7a97b-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="7a97b-110">Excel espera que **xlAddInManagerInfo12** devuelva un tipo de datos **XLOPER12** , mientras que **xlAddInManagerInfo** debe devolver un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="7a97b-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="7a97b-111">Las versiones de Excel anteriores a Excel 2007 no llaman a la función **xlAddInManagerInfo12** , ya que no son compatibles con **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="7a97b-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="7a97b-112">Excel no requiere un XLL que implemente y exporte cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="7a97b-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="7a97b-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="7a97b-113">Parameters</span></span>

 <span data-ttu-id="7a97b-114">_pxAction:_ Un puntero a un **XLOPER o XLOPER12** numérico (**xltypeInt** o **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="7a97b-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="7a97b-115">La información que Excel solicita.</span><span class="sxs-lookup"><span data-stu-id="7a97b-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7a97b-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a97b-116">Property value/Return value</span></span>

<span data-ttu-id="7a97b-117">Si _pxAction_ es o se puede convertir en el número 1, la implementación de esta función debe devolver una cadena que contenga información sobre el complemento, normalmente su nombre y quizá un número de versión.</span><span class="sxs-lookup"><span data-stu-id="7a97b-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="7a97b-118">De lo contrario, debe devolver #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="7a97b-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="7a97b-119">Si no devuelve una cadena, Excel intenta convertir el valor devuelto en una cadena.</span><span class="sxs-lookup"><span data-stu-id="7a97b-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a97b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a97b-120">Remarks</span></span>

<span data-ttu-id="7a97b-121">Si la cadena devuelta apunta a un búfer asignado dinámicamente, debe asegurarse de que este búfer se libere finalmente.</span><span class="sxs-lookup"><span data-stu-id="7a97b-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="7a97b-122">Si la cadena fue asignada por Excel, puede hacerlo estableciendo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="7a97b-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="7a97b-123">Si la cadena fue asignada por la DLL, para ello, se establece **xlbitDLLFree**y también se debe implementar en [xlAutoFree](xlautofree-xlautofree12.md) (si se va a devolver un **XLOPER**) o **xlAutoFree12** (si se va a devolver un **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="7a97b-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="7a97b-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a97b-124">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="7a97b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a97b-125">See also</span></span>



[<span data-ttu-id="7a97b-126">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="7a97b-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

