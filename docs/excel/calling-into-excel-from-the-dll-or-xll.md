---
title: Llamar a Excel desde el DLL o XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cuadros de diálogo [excel 2007], invocar comandos de excel,DLL [Excel 2007], llamar a Excel,pasar argumentos a funciones API C [Excel 2007],comandos [Excel 2007],invocar con cuadros de diálogo,comandos [Excel 2007],accesibles desde DLL o XLL,función de Excel4,función de Excel12 [Excel 2007],función de XLCallVer [Excel 2007],argumento operRes [Excel 2007],funciones [Excel 2007], accesibles desde DLL o XLL,función de Excel12v [Excel 2007], funciones solo DLL [Excel 2007],API de C [Excel 2007],pasar argumentos,argumento de número [Excel 2007],comandos [Excel 2007], llamar a versiones internacionales, comandos solo DLL [Excel 2007],versiones internacionales [Excel 2007],llamar a funciones y comandos,XLL [Excel 2007], llamar a Excel,función de Excel 4v [ Excel 2007],argumento xlfn [Excel 2007],funciones [Excel 2007], llamar a versiones internacionales
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726123"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="9879f-104">Llamar a Excel desde el DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="9879f-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="9879f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9879f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9879f-106">Microsoft Excel permite que el DLL tenga acceso a comandos de Excel integrados, funciones de hoja de cálculo y funciones de hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="9879f-106">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions.</span></span> <span data-ttu-id="9879f-107">Están disponibles en los comandos de DLL y las funciones que se llaman desde Visual Basic para Aplicaciones (VBA), así como en las funciones y los comandos XLL registrados que Excel llama directamente.</span><span class="sxs-lookup"><span data-stu-id="9879f-107">These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="9879f-108">Funciones de Excel4, Excel4v, Excel12 y Excel12v</span><span class="sxs-lookup"><span data-stu-id="9879f-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="9879f-109">Excel permite que el DLL tenga acceso a los comandos y las funciones a través de las funciones de devolución de llamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md) y [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="9879f-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="9879f-110">Las funciones de **Excel4** y **Excel4v** se introdujeron en la versión 4 de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="9879f-111">Trabajar con la estructura de datos **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="9879f-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="9879f-112">Excel 2007 introdujo dos nuevas funciones de devolución de llamada, **Excel12** y **Excel12v**, que trabajan con a estructura de datos **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9879f-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="9879f-113">Las funciones de **Excel4** y **Excel4v** se exportan mediante la biblioteca Xlcall32.lib, que debe incluirse en el proyecto DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="9879f-114">**Excel12** y **Excel12v** se incluyen en el archivo de origen del SDK para C++ Xlcall.cpp, el cual debe incluirse en el proyecto si desea obtener acceso a las funciones de Excel mediante estructuras **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9879f-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="9879f-115">El siguiente código muestra los prototipos de función para estas cuatro funciones.</span><span class="sxs-lookup"><span data-stu-id="9879f-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="9879f-116">Los primeros tres argumentos son los mismos, excepto que el segundo argumento es un puntero a una estructura **XLOPER** en el primer par y un puntero a una estructura **XLOPER12** en el segundo par.</span><span class="sxs-lookup"><span data-stu-id="9879f-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="9879f-117">La convención de llamada es **_cdecl** en **Excel4** y **Excel12** para permitir las listas de argumentos variables.</span><span class="sxs-lookup"><span data-stu-id="9879f-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="9879f-118">Los puntos suspensivos representan punteros a valores de **XLOPER** para **Excel4** y valores de **XLOPER12** para **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="9879f-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="9879f-119">El número de punteros es igual al valor del parámetro de _recuento_.</span><span class="sxs-lookup"><span data-stu-id="9879f-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="9879f-120">**Todas las versiones de Excel**</span><span class="sxs-lookup"><span data-stu-id="9879f-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="9879f-121">**A partir de Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="9879f-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="9879f-122">Para que el DLL pueda llamar a **Excel4**, **Excel4v**, **Excel12** o **Excel12v**, Excel debe pasar el control al DLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="9879f-123">Esto significa que es posible llamar a estas devoluciones de llamada de API C únicamente en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="9879f-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="9879f-124">Desde un comando XLL al que Excel llamó directamente o a través de VBA.</span><span class="sxs-lookup"><span data-stu-id="9879f-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="9879f-125">Desde una hoja de cálculo XLL o una función de hoja de macros que Excel llamó directamente o a través de VBA.</span><span class="sxs-lookup"><span data-stu-id="9879f-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="9879f-126">No puede llamar a la API C de Excel en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="9879f-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="9879f-127">Desde un evento de sistema operativo (por ejemplo, desde la función [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)).</span><span class="sxs-lookup"><span data-stu-id="9879f-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="9879f-128">Desde un proceso en segundo plano que haya creado el DLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="9879f-129">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9879f-129">Return values</span></span>

<span data-ttu-id="9879f-130">Las cuatro funciones devuelven un valor entero que informa al autor de llamada si fue posible llamar correctamente a la función o al comando.</span><span class="sxs-lookup"><span data-stu-id="9879f-130">All four of these functions return an integer value that informs the caller whether the function or command was called successfully.</span></span> <span data-ttu-id="9879f-131">Los valores devueltos pueden ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9879f-131">The returned string can be one of the following values: , , or .</span></span>
  
|<span data-ttu-id="9879f-132">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="9879f-132">**Return value**</span></span>|<span data-ttu-id="9879f-133">**Definido en Xlcall.h como**</span><span class="sxs-lookup"><span data-stu-id="9879f-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="9879f-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9879f-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9879f-135">0</span><span class="sxs-lookup"><span data-stu-id="9879f-135">(0)</span></span>  <br/> |<span data-ttu-id="9879f-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="9879f-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="9879f-137">La función o el comando se ejecutaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="9879f-137">The function or command executed successfully.</span></span> <span data-ttu-id="9879f-138">Esto no significa que la ejecución haya estado exenta de errores.</span><span class="sxs-lookup"><span data-stu-id="9879f-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="9879f-139">Por ejemplo, **Excel4** pudo devolver **xlretSuccess** cuando llamó a la función **FIND**, aunque la evaluó como **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="9879f-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="9879f-140">porque no se encontró el texto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9879f-140">because the search text could not be found.</span></span> <span data-ttu-id="9879f-141">Es necesario inspeccionar el tipo y el valor devuelto **XLOPER o XLOPER12** cuando es posible.</span><span class="sxs-lookup"><span data-stu-id="9879f-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="9879f-142">1</span><span class="sxs-lookup"><span data-stu-id="9879f-142">-1</span></span>  <br/> |<span data-ttu-id="9879f-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="9879f-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="9879f-144">El usuario detuvo una macro de comando al hacer clic en el botón **CANCELAR** o presionar la tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="9879f-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="9879f-145">2</span><span class="sxs-lookup"><span data-stu-id="9879f-145">-2</span></span>  <br/> |<span data-ttu-id="9879f-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="9879f-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="9879f-147">El código de comando o la función especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="9879f-147">The supplied function or command code is not valid.</span></span> <span data-ttu-id="9879f-148">Este error puede ocurrir cuando la función de llamada no tiene permiso para llamar a la función o el comando.</span><span class="sxs-lookup"><span data-stu-id="9879f-148">This error can occur when the calling function does not have permission to call the function or command.</span></span> <span data-ttu-id="9879f-149">Por ejemplo, una función de hoja de cálculo no puede llamar a una función de comando o una función de información de hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="9879f-149">For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="9879f-150">4</span><span class="sxs-lookup"><span data-stu-id="9879f-150">4\*</span></span>  <br/> |<span data-ttu-id="9879f-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="9879f-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="9879f-152">El número de argumentos proporcionados en la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="9879f-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="9879f-153">8</span><span class="sxs-lookup"><span data-stu-id="9879f-153">8\*</span></span>  <br/> |<span data-ttu-id="9879f-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="9879f-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="9879f-155">Uno o más de los valores del argumento **XLOPER** o **XLOPER12** no están formados o rellenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="9879f-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="9879f-156">16</span><span class="sxs-lookup"><span data-stu-id="9879f-156">1.6</span></span>  <br/> |<span data-ttu-id="9879f-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="9879f-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="9879f-158">Excel detectó un riesgo en la operación de desbordamiento de su pila y, por lo tanto, no llamó a la función.</span><span class="sxs-lookup"><span data-stu-id="9879f-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="9879f-159">32</span><span class="sxs-lookup"><span data-stu-id="9879f-159">32\*\*</span></span>  <br/> |<span data-ttu-id="9879f-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="9879f-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="9879f-161">Se produjo un error en el comando o la función por un motivo que no se describe en uno de los demás valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="9879f-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="9879f-162">Una operación que necesita una gran cantidad de memoria, por ejemplo, podría generar este error.</span><span class="sxs-lookup"><span data-stu-id="9879f-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="9879f-163">Esto puede ocurrir durante un intento de convertir una enorme referencia en una matriz **xltypeMulti** mediante la función [xlCoerce](xlcoerce.md).</span><span class="sxs-lookup"><span data-stu-id="9879f-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.</span></span>  <br/> |
|<span data-ttu-id="9879f-164">64</span><span class="sxs-lookup"><span data-stu-id="9879f-164">6.4</span></span>  <br/> |<span data-ttu-id="9879f-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="9879f-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="9879f-166">La operación intentó recuperar el valor de una celda no actualizada.</span><span class="sxs-lookup"><span data-stu-id="9879f-166">The operation attempted to retrieve the value of an uncalculated cell.</span></span> <span data-ttu-id="9879f-167">Para mantener la integridad de actualización de Excel, no se permite que las funciones de la hoja de cálculo lo hagan.</span><span class="sxs-lookup"><span data-stu-id="9879f-167">To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this.</span></span> <span data-ttu-id="9879f-168">Sin embargo, las funciones y los comandos XLL registrados como funciones de hoja de macros puedan obtener acceso a los valores de celdas no actualizadas.</span><span class="sxs-lookup"><span data-stu-id="9879f-168">However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="9879f-169">128</span><span class="sxs-lookup"><span data-stu-id="9879f-169">128 bits</span></span>  <br/> |<span data-ttu-id="9879f-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="9879f-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="9879f-171">(A partir de Excel 2007) Una función de hoja de cálculo XLL registrada como segura para subprocesos intentó llamar a una función de la API de C que no es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9879f-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="9879f-172">Por ejemplo, una función segura para subprocesos no puede llamar a la función XLM **xlfGetCell**.</span><span class="sxs-lookup"><span data-stu-id="9879f-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="9879f-173">256</span><span class="sxs-lookup"><span data-stu-id="9879f-173">256
(&H100)</span></span>  <br/> |<span data-ttu-id="9879f-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="9879f-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="9879f-175">(A partir de Excel 2010) El controlador de la función asincrónica no es válido.</span><span class="sxs-lookup"><span data-stu-id="9879f-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="9879f-176">512</span><span class="sxs-lookup"><span data-stu-id="9879f-176">5.12</span></span>  <br/> |<span data-ttu-id="9879f-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="9879f-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="9879f-178">(A partir de Excel 2010) No se admite la llamada en clústeres.</span><span class="sxs-lookup"><span data-stu-id="9879f-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="9879f-179">Si la función devuelve uno de los valores de error en la tabla (es decir, no devuelve **xlretSuccess**), el valor devuelto **XLOPER** o **XLOPER12** también se establecerá en **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="9879f-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="9879f-180">En determinadas circunstancias, comprobarlo puede ser una prueba suficiente de éxito, pero tenga en cuenta que una llamada puede devolver tanto **xlretSuccess** como **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="9879f-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="9879f-181">Si una llamada a la API C da como resultado **xlretUncalced** o **xlretAbort**, el código de DLL o XLL debe devolver control a Excel antes de realizar cualquier otra llamada a la API C (además de las llamadas a la función [xlfree ](xlfree.md) para liberar recursos de memoria asignados a Excel en los valores **XLOPER** y **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="9879f-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="9879f-182">Argumento de enumeración de funciones o comandos: xlfn</span><span class="sxs-lookup"><span data-stu-id="9879f-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="9879f-183">El argumento _xlfn_ es el primer argumento de las funciones de devolución de llamada y es un entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9879f-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="9879f-184">El valor debe ser una de las enumeraciones de comandos o funciones definidas en el archivo de encabezado del SDK Xlcall.h, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9879f-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="9879f-185">Todas las funciones de la hoja de macros y la hoja de cálculo están comprendidas entre 0 (**xlfCount**) y 0x0fff hexadecimal, aunque el mayor número asignado en Excel 2013 es 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="9879f-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="9879f-186">Todas las funciones de comandos están comprendidas entre 0x8000 hexadecimal (**xlcBeep**) y 0x8fff hexadecimal, aunque el mayor número asignado en Excel 2013 es 0x8328 hexadecimal (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="9879f-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="9879f-187">Se definen en el archivo de encabezado como `(n | xlCommand)`, donde `n` es un número decimal mayor o igual que 0 y **xlCommand** se define como 0x8000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9879f-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="9879f-188">Invocar comandos de Excel que usan cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="9879f-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="9879f-189">Algunos de los códigos de comando corresponden a las acciones en Excel que usan cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9879f-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="9879f-190">Por ejemplo, **xlcFileDelete** toma un solo argumento: un nombre de archivo o una máscara.</span><span class="sxs-lookup"><span data-stu-id="9879f-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="9879f-191">Esto se puede invocar con el cuadro de diálogo para que el usuario tenga la oportunidad de cancelar o modificar la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="9879f-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="9879f-192">También se puede llamar sin el cuadro de diálogo, en cuyo caso el archivo o los archivos se eliminan sin mayor interacción, suponiendo que existen y que al autor de llamada tiene permiso.</span><span class="sxs-lookup"><span data-stu-id="9879f-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="9879f-193">Para llamar a estos comandos en su forma de cuadro de diálogo, la enumeración de comandos debe combinarse mediante la operación bit a bit OR con 0x1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="9879f-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="9879f-194">El siguiente ejemplo de código elimina archivos en el directorio actual que coinciden con la máscara my_data\*.bak y muestra un cuadro de diálogo solo si el argumento es verdadero.</span><span class="sxs-lookup"><span data-stu-id="9879f-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="9879f-195">Llamar a funciones y comandos en versiones internacionales</span><span class="sxs-lookup"><span data-stu-id="9879f-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="9879f-196">Puede configurar Excel para mostrar los nombres de comandos XLM y funciones en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="9879f-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="9879f-197">Algunas funciones y comandos de la API de C operan en cadenas que se interpretan como nombres de comandos o funciones.</span><span class="sxs-lookup"><span data-stu-id="9879f-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="9879f-198">Por ejemplo, **xlcFormula** acepta un argumento de cadena que está pensado para colocarse en una celda especificada.</span><span class="sxs-lookup"><span data-stu-id="9879f-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="9879f-199">Para que el complemento funcione con todas las opciones de idioma, puede proporcionar los nombres de la cadena en inglés y establecer el bit 0x2000 (**xlIntl**) en la enumeración de comandos o funciones.</span><span class="sxs-lookup"><span data-stu-id="9879f-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="9879f-200">En el siguiente ejemplo de código se coloca el equivalente a `=SUM(X1:X100)` en la celda A2 de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="9879f-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="9879f-201">Tenga en cuenta que se usa la función Framework, **TempActiveRef**, para crear una referencia externa temporal **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="9879f-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="9879f-202">La fórmula aparecerá en A2 en el idioma correcto determinado por la configuración regional (por ejemplo, `=SOMME(X1:X100)` si el idioma es francés).</span><span class="sxs-lookup"><span data-stu-id="9879f-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="9879f-203">Como el resultado de la llamada a **Excel12** no es necesario, podría pasarse cero (NULL) como segundo argumento en lugar de la dirección de **xResult**.</span><span class="sxs-lookup"><span data-stu-id="9879f-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="9879f-204">Esto se describe con más detalle en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="9879f-204">( is discussed in the next section.)</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="9879f-205">Comandos y funciones solo de DLL</span><span class="sxs-lookup"><span data-stu-id="9879f-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="9879f-206">Excel admite un número reducido de funciones que solo son accesibles desde un DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="9879f-207">Se definen en el archivo de encabezado como `(n | xlSpecial)`, donde `n` es un número decimal mayor o igual que 0 y `xlSpecial` se define como 0x4000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9879f-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="9879f-208">Estas funciones se enumeran en la siguiente tabla y se documentan en la [Referencia de la función de API](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9879f-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="9879f-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="9879f-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="9879f-210">0</span><span class="sxs-lookup"><span data-stu-id="9879f-210">(0)</span></span> | <span data-ttu-id="9879f-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-212">Libera los recursos de memoria asignados por Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="9879f-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="9879f-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="9879f-214">1</span><span class="sxs-lookup"><span data-stu-id="9879f-214">-1</span></span> | <span data-ttu-id="9879f-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-216">Devuelve el espacio disponible en la pila de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="9879f-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="9879f-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="9879f-218">2</span><span class="sxs-lookup"><span data-stu-id="9879f-218">-2</span></span> | <span data-ttu-id="9879f-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-220">Convierte entre tipos de **XLOPER** y **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="9879f-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="9879f-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="9879f-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="9879f-222">3</span><span class="sxs-lookup"><span data-stu-id="9879f-222">-3</span></span> | <span data-ttu-id="9879f-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-224">Proporciona un método rápido para establecer los valores de celda.</span><span class="sxs-lookup"><span data-stu-id="9879f-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="9879f-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="9879f-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="9879f-226">4</span><span class="sxs-lookup"><span data-stu-id="9879f-226">4\*</span></span> | <span data-ttu-id="9879f-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-228">Obtiene un nombre de hoja de cálculo a partir de su identificador interno.</span><span class="sxs-lookup"><span data-stu-id="9879f-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="9879f-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="9879f-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="9879f-230">5</span><span class="sxs-lookup"><span data-stu-id="9879f-230">$-5</span></span> | <span data-ttu-id="9879f-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-232">Obtiene un identificador interno de hoja de cálculo a partir de su nombre.</span><span class="sxs-lookup"><span data-stu-id="9879f-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="9879f-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="9879f-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="9879f-234">6</span><span class="sxs-lookup"><span data-stu-id="9879f-234">-6</span></span> | <span data-ttu-id="9879f-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-236">Comprueba si el usuario hizo clic en el botón **CANCELAR** o presionó la tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="9879f-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="9879f-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="9879f-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="9879f-238">7</span><span class="sxs-lookup"><span data-stu-id="9879f-238">-7</span></span> | <span data-ttu-id="9879f-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-240">Obtiene el identificador de instancia de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="9879f-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="9879f-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="9879f-242">8</span><span class="sxs-lookup"><span data-stu-id="9879f-242">8\*</span></span> | <span data-ttu-id="9879f-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-244">Obtiene el identificador de ventana principal de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="9879f-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="9879f-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="9879f-246">9</span><span class="sxs-lookup"><span data-stu-id="9879f-246">-9</span></span> | <span data-ttu-id="9879f-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-248">Obtiene la ruta de acceso y el nombre de archivo del DLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-248">Gets the path and file name of the Visual Report template. Read-only String .</span></span>  <br/> |
|[<span data-ttu-id="9879f-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="9879f-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="9879f-250">10</span><span class="sxs-lookup"><span data-stu-id="9879f-250">1.0</span></span> | <span data-ttu-id="9879f-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-252">Esta función está en desuso y ya no es necesario llamarla.</span><span class="sxs-lookup"><span data-stu-id="9879f-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="9879f-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="9879f-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="9879f-254">11</span><span class="sxs-lookup"><span data-stu-id="9879f-254">1.1</span></span> | <span data-ttu-id="9879f-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-256">Esta función está en desuso y ya no es necesario llamarla.</span><span class="sxs-lookup"><span data-stu-id="9879f-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="9879f-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="9879f-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="9879f-258">12</span><span class="sxs-lookup"><span data-stu-id="9879f-258">1.2</span></span> | <span data-ttu-id="9879f-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-260">Define un nombre de almacenamiento binario permanente.</span><span class="sxs-lookup"><span data-stu-id="9879f-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="9879f-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="9879f-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="9879f-262">13</span><span class="sxs-lookup"><span data-stu-id="9879f-262">1.3</span></span> | <span data-ttu-id="9879f-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="9879f-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="9879f-264">Obtiene datos de un nombre de almacenamiento binario permanente.</span><span class="sxs-lookup"><span data-stu-id="9879f-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="9879f-265">Devuelve el valor XLOPER o XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="9879f-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="9879f-266">El argumento _operRes_ es el segundo argumento para las devoluciones de llamadas y es un puntero a un **XLOPER** (**Excel4** y **Excel4v**) o \*\* XLOPER12\*\* (**Excel12** y **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="9879f-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="9879f-267">Después de una llamada correcta, contiene el valor devuelto de la función o el comando.</span><span class="sxs-lookup"><span data-stu-id="9879f-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="9879f-268">**operRes** puede establecerse en cero (puntero nulo) si no se requiere ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9879f-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="9879f-269">El contenido anterior de **operRes** se sobrescribe para poder liberar antes toda la memoria a la que se apuntó previamente a fin de evitar pérdidas de memoria en la llamada.</span><span class="sxs-lookup"><span data-stu-id="9879f-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="9879f-270">Si no es posible llamar a la función o el comando (por ejemplo, si los argumentos son incorrectos), **operRes** se establece en el error **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="9879f-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="9879f-271">Un comando siempre devuelve un valor **booleano** **TRUE** si funciona correctamente o **FALSE** si se produjo un error o el usuario lo canceló.</span><span class="sxs-lookup"><span data-stu-id="9879f-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="9879f-272">Número de argumentos siguientes: count</span><span class="sxs-lookup"><span data-stu-id="9879f-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="9879f-273">El argumento _count_ es el tercer argumento de las devoluciones de llamada y es un entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9879f-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="9879f-274">Se debe establecer en el número de argumentos siguientes, a partir de 1.</span><span class="sxs-lookup"><span data-stu-id="9879f-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="9879f-275">Si un comando o una función no recibe argumentos, debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="9879f-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="9879f-276">En Microsoft Office Excel 2003, el número máximo de argumentos que puede recibir cualquier función es 30, aunque la mayoría reciben menos.</span><span class="sxs-lookup"><span data-stu-id="9879f-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="9879f-277">A partir de Excel 2007, se aumenta el número máximo de argumentos que puede recibir cualquier función a 255.</span><span class="sxs-lookup"><span data-stu-id="9879f-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="9879f-278">Con **Excel4** y **Excel12**, _count_ es el número de punteros a los valores **XLOPER** o **XLOPER12** que se pasan.</span><span class="sxs-lookup"><span data-stu-id="9879f-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="9879f-279">Debe tener cuidado de no a pasar menos argumentos que el valor en el que se establece _count_.</span><span class="sxs-lookup"><span data-stu-id="9879f-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="9879f-280">Esto provocaría que Excel siga leyendo en la pila e intente procesar valores **XLOPER** o **XLOPER12** no válidos, lo que podría bloquear la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9879f-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="9879f-281">Con **Excel4v** y **Excel12v**, _count_ es el tamaño de la matriz de punteros a los valores **XLOPER** o **XLOPER12** que se pasan como el argumento siguiente y final.</span><span class="sxs-lookup"><span data-stu-id="9879f-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="9879f-282">De nuevo, debe tener cuidado de no pasar una matriz menor que _count_ elementos en tamaño, ya que esto provocará la saturación de los límites de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9879f-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="9879f-283">Pasar argumentos a las funciones de la API de C</span><span class="sxs-lookup"><span data-stu-id="9879f-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="9879f-284">Tanto **Excel4** como **Excel12** toman listas de argumentos de longitud variable, después de _count_, que se interpretan como punteros a los valores **XLOPER** y **XLOPER12**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9879f-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="9879f-285">**Excel4v** y **Excel12v** reciben un solo argumento, después de _count_, que es un puntero a una matriz de punteros a los valores **XLOPER** en el caso de **Excel4v** y a los valores **XLOPER12** en el caso de **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="9879f-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="9879f-286">Los formularios de matriz, **Excel4v** y **Excel12v**, le permiten programar una llamada a la API de C de forma nítida cuando el número de argumentos es variable.</span><span class="sxs-lookup"><span data-stu-id="9879f-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="9879f-287">El siguiente ejemplo muestra una función que toma una matriz de números de tamaño variable y usa las funciones de hoja de cálculo de Excel, mediante la API de C, para calcular la suma, el promedio, el mínimo y el máximo.</span><span class="sxs-lookup"><span data-stu-id="9879f-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="9879f-288">Reemplazar las referencias a los valores **XLOPER12** con **XLOPER** y **Excel12v** con **Excel4v**, en el código anterior tendría como resultado una función compatible con todas las versiones de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="9879f-289">Esta operación de las funciones de Excel **SUMA**, **PROMEDIO**, **MIN** y **MÁX** es bastante sencilla por lo que sería más eficaz programarlas en C y evitar la sobrecarga de preparar los argumentos y llamar a Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="9879f-290">Sin embargo, muchas de las funciones que contiene Excel son más complejas, por lo que este método es útil en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="9879f-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="9879f-291">El tema sobre [xlfRegister](xlfregister-form-1.md) proporciona otro ejemplo de trabajo con **Excel4v** y **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="9879f-291">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="9879f-292">Cuando se registra una función de hoja de cálculo XLL, puede proporcionar una cadena descriptiva para cada argumento que se usa en el cuadro de diálogo **Pegar función**.</span><span class="sxs-lookup"><span data-stu-id="9879f-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="9879f-293">Por lo tanto, el número de argumentos totales que se proporciona a **xlfRegister** depende del número de argumentos que acepta la función XLL y puede variar de una función a otra.</span><span class="sxs-lookup"><span data-stu-id="9879f-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="9879f-294">Si siempre llama a una función de la API de C o un comando con el mismo número de argumentos, querrá evitar el paso adicional de la creación de una matriz de punteros para esos argumentos.</span><span class="sxs-lookup"><span data-stu-id="9879f-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="9879f-295">En esos casos, es más sencillo y más claro usar **Excel4** y **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="9879f-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="9879f-296">Por ejemplo, al registrar los comandos y las funciones XLL, debe proporcionar la ruta de acceso completa y el nombre de archivo del DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="9879f-297">Puede obtener el nombre de archivo en una llamada a **xlfGetName** y después liberarlo con una llamada a **xlFree**, tal como se muestra en el ejemplo siguiente para **Excel4** y \*\* Excel12\*\*.</span><span class="sxs-lookup"><span data-stu-id="9879f-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="9879f-298">En la práctica, la función **Excel12v_example**, podría codificarse de forma más eficiente creando un solo argumento **xltypeMulti** **XLOPER12** y llamando a la API de C mediante **Excel12**, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9879f-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="9879f-299">En este caso, el valor devuelto de **Excel12** se pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="9879f-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="9879f-300">En su lugar, el código comprueba que el valor **XLOPER12** devuelto sea **xltypeNum** para determinar si la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9879f-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="9879f-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="9879f-301">XLCallVer</span></span>

<span data-ttu-id="9879f-302">Además de las devoluciones de llamada a **Excel4**, **Excel4v**, **Excel12** y **Excel12v**, Excel exporta una función \*\* XLCallVer\*\*, que devuelve la versión de la API de C actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="9879f-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="9879f-303">El prototipo de la función es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="9879f-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="9879f-304">Puede llamar a esta función, que es segura para subprocesos, desde cualquier función o comando XLL.</span><span class="sxs-lookup"><span data-stu-id="9879f-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="9879f-305">En Excel 97 a Excel 2003, **XLCallVer** devuelve 1280 = 0x0500 hex = 5 x 256, que indica la versión 5 de Excel.</span><span class="sxs-lookup"><span data-stu-id="9879f-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="9879f-306">A partir de Excel 2007, devuelve 3072 = 0x0c00 hex = 12 x 256, que asimismo indica la versión 12.</span><span class="sxs-lookup"><span data-stu-id="9879f-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="9879f-307">Aunque puede usar esto para determinar si la nueva API de C está disponible en tiempo de ejecución, tal vez prefiera detectar la versión en ejecución de Excel mediante `Excel4(xlfGetWorkspace, &version, 1, &arg)`, donde `arg` es un valor **XLOPER** numérico que se establece en 2.</span><span class="sxs-lookup"><span data-stu-id="9879f-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="9879f-308">La función devuelve una cadena **XLOPER**, versión, que después puede convertirse en un entero.</span><span class="sxs-lookup"><span data-stu-id="9879f-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="9879f-309">Las razones para depender de la versión de Excel en lugar de la versión de la API de C es que hay diferencias entre Excel 2000, Excel 2002 y Excel 2003 que tal vez el complemento necesite detectar también.</span><span class="sxs-lookup"><span data-stu-id="9879f-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="9879f-310">Por ejemplo, los cambios realizados en la precisión de algunas de las funciones estadísticas.</span><span class="sxs-lookup"><span data-stu-id="9879f-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9879f-311">Vea también</span><span class="sxs-lookup"><span data-stu-id="9879f-311">See also</span></span>

- [<span data-ttu-id="9879f-312">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="9879f-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="9879f-313">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="9879f-313">Accessing XLL code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="9879f-314">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="9879f-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="9879f-315">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="9879f-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="9879f-316">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="9879f-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

