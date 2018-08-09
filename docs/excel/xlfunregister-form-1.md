---
title: xlfUnregister (Formulario 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister (función) [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815735"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="657b4-104">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="657b4-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="657b4-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="657b4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="657b4-106">Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="657b4-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="657b4-107">Esto equivale a llamar al **Cancelar el registro** de una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="657b4-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="657b4-108">**xlfUnregister** se puede llamar de dos formas:</span><span class="sxs-lookup"><span data-stu-id="657b4-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="657b4-109">Formulario 1: Anula el registro de un comando individual o una función.</span><span class="sxs-lookup"><span data-stu-id="657b4-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="657b4-110">Formulario 2: Descarga y desactiva un XLL.</span><span class="sxs-lookup"><span data-stu-id="657b4-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="657b4-111">Se llama en el formulario 1, esta función reduce el recuento de uso de una función DLL o el comando que se registró anteriormente con **xlfRegister** o **registrar**.</span><span class="sxs-lookup"><span data-stu-id="657b4-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="657b4-112">Si el contador de uso ya es cero, esta función no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="657b4-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="657b4-113">Cuando el recuento de uso de todas las funciones en un archivo DLL llega a cero, el archivo DLL se descargue de la memoria.</span><span class="sxs-lookup"><span data-stu-id="657b4-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="657b4-114">**xlfRegister** (Formulario número 1) también define un nombre oculto que es el argumento de texto de la función, _pxFunctionText_, y que se evalúa como a la función o el identificador de registro. del comando</span><span class="sxs-lookup"><span data-stu-id="657b4-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="657b4-115">Cuando la anulación del registro de la función, este nombre se debe eliminar con **xlfSetName** de forma que ya no aparece el nombre de función mediante el Asistente para la función.</span><span class="sxs-lookup"><span data-stu-id="657b4-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="657b4-116">Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="657b4-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="657b4-117">Parámetros</span><span class="sxs-lookup"><span data-stu-id="657b4-117">Parameters</span></span>

<span data-ttu-id="657b4-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="657b4-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="657b4-119">El identificador de registro de la función se va a anular.</span><span class="sxs-lookup"><span data-stu-id="657b4-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="657b4-120">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="657b4-120">Property value/Return value</span></span>

<span data-ttu-id="657b4-121">Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**), en caso contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="657b4-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="657b4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="657b4-122">Remarks</span></span>

<span data-ttu-id="657b4-123">El registro del que identificador de la función es devuelto por **xlfRegister** cuando la función es el primera registrado.</span><span class="sxs-lookup"><span data-stu-id="657b4-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="657b4-124">También puede obtenerse mediante una llamada a la [función xlfRegisterId](xlfregisterid.md) o la [función xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="657b4-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="657b4-125">Tenga en cuenta que xlfRegisterId intenta registrar la función si todavía no se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="657b4-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="657b4-126">Por este motivo, si sólo está intentando obtener el identificador de modo que puede anular el registro de la función, es mejor obtener pasando el nombre registrado para **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="657b4-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="657b4-127">¿Si la función no se ha registrado, se produce un error en la **xlfEvaluate** con una #NAME? error.</span><span class="sxs-lookup"><span data-stu-id="657b4-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="657b4-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="657b4-128">Example</span></span>

<span data-ttu-id="657b4-129">Vea el código para la función **fExit** en `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="657b4-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="657b4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="657b4-130">See also</span></span>

- [<span data-ttu-id="657b4-131">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="657b4-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="657b4-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="657b4-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="657b4-133">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="657b4-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="657b4-134">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="657b4-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

