---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- función excel12v [excel 2007],función Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414994"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="09841-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="09841-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="09841-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="09841-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="09841-106">Llama a una función Microsoft Excel hoja de cálculo interna, una función o un comando de hoja de macros o un comando especial de XLL desde un recurso dll, XLL o código.</span><span class="sxs-lookup"><span data-stu-id="09841-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="09841-107">Todas las versiones recientes de Excel **admiten Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="09841-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="09841-108">A partir Excel 2007, **se admite Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="09841-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="09841-109">Estas funciones solo se pueden llamar cuando Excel ha pasado el control a la DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="09841-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="09841-110">También se pueden llamar cuando Excel ha pasado el control indirectamente a través de una llamada a Visual Basic para Aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="09841-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="09841-111">No se puede llamar a ellos en otro momento.</span><span class="sxs-lookup"><span data-stu-id="09841-111">They cannot be called at any other time.</span></span> <span data-ttu-id="09841-112">Por ejemplo, no se puede llamar a ellos durante las llamadas a la función DllMain u otras veces en las que el sistema operativo haya llamado a la DLL o desde un subproceso creado por el DLL.</span><span class="sxs-lookup"><span data-stu-id="09841-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="09841-113">Las funciones de Excel4 y [Excel12](excel4-excel12.md) aceptan sus argumentos como una lista de longitud variable en la pila, mientras que las funciones **Excel4v** y **Excel12v** aceptan sus argumentos como una matriz.</span><span class="sxs-lookup"><span data-stu-id="09841-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="09841-114">En todos los demás aspectos, **Excel4** se comporta igual que **Excel4v** y **Excel12** se comporta igual que **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="09841-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="09841-115">Parameters</span><span class="sxs-lookup"><span data-stu-id="09841-115">Parameters</span></span>

 <span data-ttu-id="09841-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="09841-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="09841-117">Un número que indica el comando, la función o la función especial a la que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="09841-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="09841-118">Para obtener una lista de valores  _iFunction_ válidos, consulte la sección Comentarios siguientes.</span><span class="sxs-lookup"><span data-stu-id="09841-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="09841-119">_pxRes_ (**LPXLOPER** o **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="09841-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="09841-120">Puntero a **un XLOPER** (en el caso de **Excel4v**) o a **un XLOPER12** (en el caso de **Excel12v**) que contendrán el resultado de la función evaluada.</span><span class="sxs-lookup"><span data-stu-id="09841-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="09841-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="09841-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="09841-122">Número de argumentos posteriores que se pasarán a la función.</span><span class="sxs-lookup"><span data-stu-id="09841-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="09841-123">En las versiones de Excel hasta 2003, puede ser cualquier número del 0 al 30.</span><span class="sxs-lookup"><span data-stu-id="09841-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="09841-124">A partir Excel 2007, puede ser cualquier número del 0 al 255.</span><span class="sxs-lookup"><span data-stu-id="09841-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="09841-125">_rgx_ (**LPXLOPER []** o **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="09841-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="09841-126">Matriz que contiene los argumentos de la función.</span><span class="sxs-lookup"><span data-stu-id="09841-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="09841-127">Todos los argumentos de la matriz deben ser punteros a **valores XLOPER** o **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="09841-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="09841-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09841-128">Return value</span></span>

<span data-ttu-id="09841-129">Estas funciones devuelven los mismos valores que **Excel4** y **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="09841-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09841-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09841-130">Remarks</span></span>

<span data-ttu-id="09841-131">Estas funciones son útiles cuando el número de argumentos que se pasan al operador es variable.</span><span class="sxs-lookup"><span data-stu-id="09841-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="09841-132">Por ejemplo, **Excel4v** y **Excel12v** son útiles al registrar funciones mediante [xlfRegister](xlfregister-form-1.md) donde el número de argumentos totales depende del número de argumentos tomados por la función que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="09841-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="09841-133">**Excel4v** y **Excel12v** también son útiles al escribir una función contenedora para **Excel4** o **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="09841-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="09841-134">En estos casos, debe convertir una lista de argumentos variables, como normalmente se suministraría a **Excel4** o **Excel12,** en un único argumento de matriz de tamaño variable para volver a llamar a Excel mediante **Excel4v** o **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="09841-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="09841-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09841-135">Example</span></span>

<span data-ttu-id="09841-136">Para obtener ejemplos de código, vea el código de las funciones **Excel** y **Excel12f** en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK:</span><span class="sxs-lookup"><span data-stu-id="09841-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="09841-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="09841-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09841-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="09841-138">See also</span></span>



[<span data-ttu-id="09841-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="09841-139">Excel4/Excel12</span></span>](excel4-excel12.md)

