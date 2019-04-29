---
title: xlfUnregister (Formulario 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- función xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410087"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="bd949-104">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="bd949-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="bd949-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd949-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bd949-106">Se puede llamar desde un comando DLL o XLL a los que ha llamado Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bd949-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="bd949-107">Esto equivale a llamar **unregister** desde una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="bd949-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="bd949-108">se puede llamar a **xlfUnregister** de dos formas:</span><span class="sxs-lookup"><span data-stu-id="bd949-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="bd949-109">Formulario 1: anula el registro de un comando individual o una función.</span><span class="sxs-lookup"><span data-stu-id="bd949-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="bd949-110">Formulario 2: descarga y desactiva un XLL.</span><span class="sxs-lookup"><span data-stu-id="bd949-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="bd949-111">Esta función, que se llama en el formulario 1, reduce el recuento de uso de una función o un comando DLL que se registró previamente con **xlfRegister** o **Register**.</span><span class="sxs-lookup"><span data-stu-id="bd949-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="bd949-112">Si el recuento de uso ya es cero, esta función no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="bd949-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="bd949-113">Cuando el recuento de todas las funciones de una DLL llega a cero, el archivo DLL se descarga de la memoria.</span><span class="sxs-lookup"><span data-stu-id="bd949-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="bd949-114">**xlfRegister** (Formulario 1) también define un nombre oculto que es el argumento del texto de la función, _pxFunctionText_, y que se evalúa en el identificador de registro de la función o el comando.</span><span class="sxs-lookup"><span data-stu-id="bd949-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="bd949-115">Al anular el registro de la función, este nombre debe eliminarse con **xlfSetName** de modo que el nombre de la función ya no aparezca en la lista del Asistente para funciones.</span><span class="sxs-lookup"><span data-stu-id="bd949-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="bd949-116">Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="bd949-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="bd949-117">Parameters</span><span class="sxs-lookup"><span data-stu-id="bd949-117">Parameters</span></span>

<span data-ttu-id="bd949-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="bd949-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="bd949-119">IDENTIFICADOR de registro de la función que se va a anular en el registro.</span><span class="sxs-lookup"><span data-stu-id="bd949-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bd949-120">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd949-120">Property value/Return value</span></span>

<span data-ttu-id="bd949-121">Si se ejecuta correctamente, devuelve **true** (**xltypeBool**), de lo contrario devuelve false.</span><span class="sxs-lookup"><span data-stu-id="bd949-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd949-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd949-122">Remarks</span></span>

<span data-ttu-id="bd949-123">**XlfRegister** devuelve el identificador de registro de la función cuando la función se registra por primera vez.</span><span class="sxs-lookup"><span data-stu-id="bd949-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="bd949-124">También se puede obtener llamando a la [función xlfRegisterId](xlfregisterid.md) o a la [función xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="bd949-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="bd949-125">Tenga en cuenta que xlfRegisterId intenta registrar la función si aún no se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="bd949-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="bd949-126">Por este motivo, si solo intenta obtener el identificador para que pueda anular el registro de la función, es mejor obtenerlo pasando el nombre registrado a **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="bd949-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="bd949-127">Si no se ha registrado la función, **xlfEvaluate** produce un error con un #NAME? error.</span><span class="sxs-lookup"><span data-stu-id="bd949-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bd949-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd949-128">Example</span></span>

<span data-ttu-id="bd949-129">Consulte el código de la función **fExit** en `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="bd949-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="bd949-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd949-130">See also</span></span>

- [<span data-ttu-id="bd949-131">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="bd949-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="bd949-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="bd949-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="bd949-133">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="bd949-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="bd949-134">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="bd949-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

