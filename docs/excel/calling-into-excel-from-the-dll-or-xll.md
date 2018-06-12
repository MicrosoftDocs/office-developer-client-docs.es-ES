---
title: Llamar a Excel desde el archivo DLL o XLL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- comandos, archivos DLL [Excel 2007], llamada en Excel, pasar argumentos a funciones de la API de C [Excel 2007], [Excel 2007], los comandos de excel de cuadros de diálogo [excel 2007], invocación de invocar con cuadros de diálogo, comandos [Excel 2007], accesibles desde el archivo DLL o XLL, Excel4 funcionan [ Función de Excel12 de Excel 2007], [Excel 2007], XLCallVer funcionar el argumento de operRes [Excel 2007], [Excel 2007], funciones [Excel 2007], accesibles desde el archivo DLL o XLL, Excel12v funcionan [Excel 2007], sólo DLL funciona API de C [Excel 2007], [Excel 2007], pasar recuento de argumentos, argumento [Excel 2007], comandos [Excel 2007], al llamar a las versiones internacionales, sólo DLL comandos [Excel 2007], las versiones internacionales [Excel 2007], llamada a funciones y comandos, XLL [Excel 2007], llamada a Excel, Excel 4v función [ Excel 2007], xlfn argumento [Excel 2007], [Excel 2007], funciones de llamada en las versiones internacionales
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815574"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="bb11d-104">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="bb11d-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="bb11d-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bb11d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bb11d-106">Microsoft Excel permite que el archivo DLL tener acceso a comandos integrados de Excel, funciones de hoja de cálculo y las funciones de hoja de macro.</span><span class="sxs-lookup"><span data-stu-id="bb11d-106">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions.</span></span> <span data-ttu-id="bb11d-107">Se encuentran disponibles tanto de los comandos del archivo DLL y las funciones llamadas desde Visual Basic para aplicaciones (VBA) y de funciones llamadas directamente por Excel y comandos XLL registrados.</span><span class="sxs-lookup"><span data-stu-id="bb11d-107">These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="bb11d-108">Excel4, Excel4v, Excel12 y funciones Excel12v</span><span class="sxs-lookup"><span data-stu-id="bb11d-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="bb11d-109">Excel permite que el archivo DLL tener acceso a los comandos y las funciones a través de las funciones de devolución de llamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)y [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="bb11d-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="bb11d-110">Las funciones de **Excel4** y **Excel4v** se introdujeron en Excel versión 4.</span><span class="sxs-lookup"><span data-stu-id="bb11d-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="bb11d-111">Trabajar con la estructura de datos **XLOPER** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="bb11d-112">Excel 2007 introdujo dos nuevas funciones de devolución de llamada, **Excel12** y **Excel12v**, que funcionan con la estructura de datos **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="bb11d-113">Las funciones de **Excel4** y **Excel4v** se exportan en la biblioteca de Xlcall32.lib, que debe estar incluido en el proyecto de DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="bb11d-114">**Excel12** y **Excel12v** se incluyen en el archivo de origen C++ SDK Xlcall.cpp, que se debe incluir en el proyecto si desea tener acceso a la funcionalidad de Excel mediante el uso de estructuras **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="bb11d-115">El código siguiente muestra los prototipos de función para estas cuatro funciones.</span><span class="sxs-lookup"><span data-stu-id="bb11d-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="bb11d-116">Los tres primeros argumentos son los mismos, excepto en que el segundo argumento es un puntero a un **XLOPER** en el primer par y un puntero a un **XLOPER12** en el segundo par.</span><span class="sxs-lookup"><span data-stu-id="bb11d-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="bb11d-117">La convención de llamada es **_cdecl** en **Excel4** y **Excel12** para permitir que las listas de argumentos de variable.</span><span class="sxs-lookup"><span data-stu-id="bb11d-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="bb11d-118">Los puntos suspensivos representa punteros a los valores **XLOPER** de **Excel4** y **XLOPER12** valores para **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="bb11d-119">El número de punteros es igual al valor del parámetro _count_ .</span><span class="sxs-lookup"><span data-stu-id="bb11d-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="bb11d-120">**Todas las versiones de Excel**</span><span class="sxs-lookup"><span data-stu-id="bb11d-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="bb11d-121">**Iniciar en Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="bb11d-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="bb11d-122">Para que el archivo DLL poder llamar a **Excel4**, **Excel4v**, **Excel12**o **Excel12v**, Excel debe pasar el control a la DLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="bb11d-123">Esto significa que se pueden llamar a estas devoluciones de llamada de la API C sólo en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="bb11d-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="bb11d-124">Desde un comando de XLL de Excel ha llamado directamente o a través de VBA.</span><span class="sxs-lookup"><span data-stu-id="bb11d-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="bb11d-125">Desde dentro de una función de hoja de hoja de cálculo o una macro XLL que Excel ha llamado directamente o a través de VBA.</span><span class="sxs-lookup"><span data-stu-id="bb11d-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="bb11d-126">No se puede llamar a la API de C de Excel en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="bb11d-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="bb11d-127">Desde un evento de sistema operativo (por ejemplo, de la función [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="bb11d-127">From an operating system event (for example, from the [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) function).</span></span> 
    
- <span data-ttu-id="bb11d-128">Desde un subproceso de fondo que crea el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="bb11d-129">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="bb11d-129">Return values</span></span>

<span data-ttu-id="bb11d-130">Cuatro de estas funciones devuelve un valor entero que se informa de si la función o el comando recibió correctamente el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="bb11d-130">All four of these functions return an integer value that informs the caller whether the function or command was called successfully.</span></span> <span data-ttu-id="bb11d-131">Los valores devueltos pueden ser cualquiera de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="bb11d-131">The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="bb11d-132">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="bb11d-132">**Return value**</span></span>|<span data-ttu-id="bb11d-133">**Definido en Xlcall.h como**</span><span class="sxs-lookup"><span data-stu-id="bb11d-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="bb11d-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb11d-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb11d-135">0</span><span class="sxs-lookup"><span data-stu-id="bb11d-135">0</span></span>  <br/> |<span data-ttu-id="bb11d-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="bb11d-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="bb11d-137">La función o el comando que se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-137">The function or command executed successfully.</span></span> <span data-ttu-id="bb11d-138">Esto no significa que la ejecución ha producido error gratuita.</span><span class="sxs-lookup"><span data-stu-id="bb11d-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="bb11d-139">Por ejemplo, **Excel4** podría devolver **xlretSuccess** cuando se llama a la función **Buscar**, aunque evalúan hasta **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="bb11d-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="bb11d-140">debido a que no se pudo encontrar el texto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bb11d-140">because the search text could not be found.</span></span> <span data-ttu-id="bb11d-141">Inspeccione el tipo y el valor de devuelto **XLOPER y XLOPER12** donde esto es una posibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb11d-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="bb11d-142">1</span><span class="sxs-lookup"><span data-stu-id="bb11d-142">1</span></span>  <br/> |<span data-ttu-id="bb11d-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="bb11d-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="bb11d-144">Una macro de comando se detuvo por el usuario hace clic en el botón **Cancelar** o al presionar la tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="bb11d-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="bb11d-145">2</span><span class="sxs-lookup"><span data-stu-id="bb11d-145">2</span></span>  <br/> |<span data-ttu-id="bb11d-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="bb11d-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="bb11d-147">El código de comando o función proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="bb11d-147">The supplied function or command code is not valid.</span></span> <span data-ttu-id="bb11d-148">Este error puede producirse cuando la función de llamada no tiene permiso para llamar a la función o el comando.</span><span class="sxs-lookup"><span data-stu-id="bb11d-148">This error can occur when the calling function does not have permission to call the function or command.</span></span> <span data-ttu-id="bb11d-149">Por ejemplo, una función de hoja de cálculo no puede llamar a una función de información de hoja de macro o un comando.</span><span class="sxs-lookup"><span data-stu-id="bb11d-149">For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="bb11d-150">4</span><span class="sxs-lookup"><span data-stu-id="bb11d-150">4</span></span>  <br/> |<span data-ttu-id="bb11d-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="bb11d-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="bb11d-152">El número de argumentos proporcionado en la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="bb11d-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="bb11d-153">8</span><span class="sxs-lookup"><span data-stu-id="bb11d-153">8</span></span>  <br/> |<span data-ttu-id="bb11d-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="bb11d-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="bb11d-155">Uno o varios de los valores del argumento **XLOPER** o **XLOPER12** correctamente no están formado o se rellena.</span><span class="sxs-lookup"><span data-stu-id="bb11d-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="bb11d-156">16</span><span class="sxs-lookup"><span data-stu-id="bb11d-156">16</span></span>  <br/> |<span data-ttu-id="bb11d-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="bb11d-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="bb11d-158">Excel detectó un riesgo de que la operación es posible que su pila de desbordamiento y, por lo tanto, no llame a la función.</span><span class="sxs-lookup"><span data-stu-id="bb11d-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="bb11d-159">32</span><span class="sxs-lookup"><span data-stu-id="bb11d-159">32</span></span>  <br/> |<span data-ttu-id="bb11d-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="bb11d-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="bb11d-161">El comando o la función no se pudo por un motivo no descrito por uno de los otros valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="bb11d-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="bb11d-162">Una operación que sería necesario demasiada memoria, por ejemplo, se producirá un error con este error.</span><span class="sxs-lookup"><span data-stu-id="bb11d-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="bb11d-163">Esto puede suceder durante un intento de convertir una referencia a una matriz **xltypeMulti** muy grande mediante el uso de la función [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bb11d-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) function.</span></span>  <br/> |
|<span data-ttu-id="bb11d-164">64</span><span class="sxs-lookup"><span data-stu-id="bb11d-164">64</span></span>  <br/> |<span data-ttu-id="bb11d-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="bb11d-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="bb11d-166">Se ha intentado la operación recuperar el valor de una celda no calculada.</span><span class="sxs-lookup"><span data-stu-id="bb11d-166">The operation attempted to retrieve the value of an uncalculated cell.</span></span> <span data-ttu-id="bb11d-167">Para conservar la integridad de los cálculos en Excel, funciones de hoja de cálculo no se permiten hacer esto.</span><span class="sxs-lookup"><span data-stu-id="bb11d-167">To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this.</span></span> <span data-ttu-id="bb11d-168">Sin embargo, las funciones y comandos XLL registran como funciones de hoja de macros se pueden tener acceso a los valores de celda no calculada.</span><span class="sxs-lookup"><span data-stu-id="bb11d-168">However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="bb11d-169">128</span><span class="sxs-lookup"><span data-stu-id="bb11d-169">128</span></span>  <br/> |<span data-ttu-id="bb11d-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="bb11d-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="bb11d-171">(Comenzando en Excel 2007) Una función de hoja de cálculo XLL registrada como seguros para subprocesos ha intentado llamar a una función de la API de C que no es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bb11d-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="bb11d-172">Por ejemplo, una función de subprocesos no puede llamar a la función XLM **xlfGetCell**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="bb11d-173">256</span><span class="sxs-lookup"><span data-stu-id="bb11d-173">256</span></span>  <br/> |<span data-ttu-id="bb11d-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="bb11d-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="bb11d-175">(Comenzando en Excel 2010) El identificador de función asincrónica no es válido.</span><span class="sxs-lookup"><span data-stu-id="bb11d-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="bb11d-176">512</span><span class="sxs-lookup"><span data-stu-id="bb11d-176">512</span></span>  <br/> |<span data-ttu-id="bb11d-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="bb11d-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="bb11d-178">(Comenzando en Excel 2010) La llamada no se admite en clústeres.</span><span class="sxs-lookup"><span data-stu-id="bb11d-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="bb11d-179">Si la función devuelve uno de los valores de error en la tabla (es decir, no devuelve **xlretSuccess**), el valor devuelto **XLOPER** o **XLOPER12** también se establecerá en **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="bb11d-180">En determinadas circunstancias, para esto puede resultar una prueba suficiente de éxito, pero debe tener en cuenta que una llamada puede devolver ambos **xlretSuccess** de comprobación y **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="bb11d-181">Si una llamada a los resultados de la API C en **xlretUncalced** o **xlretAbort**, el código de la DLL o XLL debe devolver el control a Excel antes de realizar otras llamadas API C (que no sean llamadas a la función [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) para liberar memoria asignada en Excel recursos en los valores **XLOPER** y **XLOPER12** ).</span><span class="sxs-lookup"><span data-stu-id="bb11d-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="bb11d-182">Comando o un argumento de función (enumeración): xlfn</span><span class="sxs-lookup"><span data-stu-id="bb11d-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="bb11d-183">El argumento _xlfn_ es el primer argumento a la devolución de llamada funciona y es un entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bb11d-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="bb11d-184">Su valor debe ser una de las enumeraciones de función o un comando definidas en el archivo de encabezado SDK Xlcall.h, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb11d-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
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

<span data-ttu-id="bb11d-185">Hoja de hoja de cálculo y de macros todas las funciones están en el intervalo entre 0 (**xlfCount**) a través de 0x0fff hexadecimal, aunque había asignado el mayor número de Excel 2013 es 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="bb11d-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="bb11d-186">Todas las funciones de comando se encuentran en el intervalo de 0 x 8000 hexadecimal (**xlcBeep**) a través de 0x8fff hexadecimal, aunque el número más alto asignado en Excel 2013 es 0x8328 hexadecimal (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="bb11d-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="bb11d-187">Se definen en el archivo de encabezado como `(n | xlCommand)` donde `n` es un número decimal mayor o igual a 0 y **xlCommand** se define como 0 x 8000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bb11d-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="bb11d-188">Invocar los comandos de Excel que utilizar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="bb11d-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="bb11d-189">Algunos de los códigos de comando corresponden a acciones en Excel que utilizar cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb11d-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="bb11d-190">Por ejemplo, **xlcFileDelete** toma un único argumento: un nombre de archivo o máscara.</span><span class="sxs-lookup"><span data-stu-id="bb11d-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="bb11d-191">Esto se puede invocar con el cuadro de diálogo para que el usuario tiene la oportunidad de cancelar o modificar la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="bb11d-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="bb11d-192">Se puede también llamar sin el cuadro de diálogo, en cuyo caso se eliminan el archivo o archivos sin interacción más, suponiendo que existan y el autor de la llamada tiene permiso.</span><span class="sxs-lookup"><span data-stu-id="bb11d-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="bb11d-193">Para llamar a esos comandos en su formulario de cuadro de diálogo, se debe combinar la enumeración de comando mediante el uso de la operación OR bit a bit con 0 x 1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="bb11d-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="bb11d-194">En el ejemplo de código siguiente se elimina los archivos en el directorio actual que coinciden con la máscara my_data\*.bak, mostrar un cuadro de diálogo sólo si el argumento es true.</span><span class="sxs-lookup"><span data-stu-id="bb11d-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="bb11d-195">Llamada a funciones y comandos de las versiones internacionales</span><span class="sxs-lookup"><span data-stu-id="bb11d-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="bb11d-196">Puede configurar Excel para mostrar las funciones y nombres de los comandos XLM en una gran variedad de idiomas.</span><span class="sxs-lookup"><span data-stu-id="bb11d-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="bb11d-197">Algunos comandos de la API de C y funciones funcionan en cadenas que se interpretan como nombres de función o un comando.</span><span class="sxs-lookup"><span data-stu-id="bb11d-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="bb11d-198">Por ejemplo, **xlcFormula** toma un argumento de cadena que está pensado para colocarse en una celda especificada.</span><span class="sxs-lookup"><span data-stu-id="bb11d-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="bb11d-199">Para el complemento para que funcione con todas las opciones de idioma, puede proporcionar los nombres de cadena en inglés y establecer el bit 0 x 2000 (**xlIntl**) en la enumeración de función o un comando.</span><span class="sxs-lookup"><span data-stu-id="bb11d-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="bb11d-200">En el ejemplo de código siguiente se coloca el equivalente de `=SUM(X1:X100)` en la celda A2 de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="bb11d-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="bb11d-201">Tenga en cuenta que usa la función de Framework, **TempActiveRef**, para crear una referencia externa temporal **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="bb11d-202">La fórmula aparecerá en A2 en el idioma correcto de determinada configuración regional (por ejemplo, `=SOMME(X1:X100)` si el idioma es francés).</span><span class="sxs-lookup"><span data-stu-id="bb11d-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
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
> <span data-ttu-id="bb11d-203">Debido a que el resultado de la llamada a **Excel12** no es necesario, se podría pasar cero (NULL) como el segundo argumento en lugar de la dirección de **xResult**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="bb11d-204">Esto se explica más en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="bb11d-204">This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="bb11d-205">Comandos y funciones sólo DLL</span><span class="sxs-lookup"><span data-stu-id="bb11d-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="bb11d-206">Excel admite un número reducido de funciones que sólo son accesibles desde una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="bb11d-207">Se definen en el archivo de encabezado como `(n | xlSpecial)` donde `n` es un número decimal mayor o igual a 0 y `xlSpecial` se define como 0 x 4000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bb11d-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="bb11d-208">Estas funciones están enumeradas en la siguiente tabla y documentadas en la [Referencia de función de la API](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bb11d-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="bb11d-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="bb11d-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="bb11d-210">0</span><span class="sxs-lookup"><span data-stu-id="bb11d-210">0</span></span> | <span data-ttu-id="bb11d-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-212">Libera los recursos de memoria asignada en Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="bb11d-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="bb11d-214">1</span><span class="sxs-lookup"><span data-stu-id="bb11d-214">1</span></span> | <span data-ttu-id="bb11d-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-216">Devuelve el espacio libre en la pila de Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="bb11d-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="bb11d-218">2</span><span class="sxs-lookup"><span data-stu-id="bb11d-218">2</span></span> | <span data-ttu-id="bb11d-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-220">Convierte entre tipos **XLOPER** y **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="bb11d-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="bb11d-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="bb11d-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="bb11d-222">3</span><span class="sxs-lookup"><span data-stu-id="bb11d-222">3</span></span> | <span data-ttu-id="bb11d-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-224">Proporciona un método rápido de establecer valores de celda.</span><span class="sxs-lookup"><span data-stu-id="bb11d-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="bb11d-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="bb11d-226">4</span><span class="sxs-lookup"><span data-stu-id="bb11d-226">4</span></span> | <span data-ttu-id="bb11d-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-228">Obtiene un nombre de hoja de cálculo de su identificador interno.</span><span class="sxs-lookup"><span data-stu-id="bb11d-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="bb11d-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="bb11d-230">5</span><span class="sxs-lookup"><span data-stu-id="bb11d-230">5</span></span> | <span data-ttu-id="bb11d-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-232">Obtiene un identificador interno de la hoja de cálculo de su nombre.</span><span class="sxs-lookup"><span data-stu-id="bb11d-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="bb11d-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="bb11d-234">6</span><span class="sxs-lookup"><span data-stu-id="bb11d-234">6</span></span> | <span data-ttu-id="bb11d-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-236">Comprueba si el usuario hizo clic en el botón **Cancelar** o presiona la tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="bb11d-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="bb11d-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="bb11d-238">7</span><span class="sxs-lookup"><span data-stu-id="bb11d-238">7</span></span> | <span data-ttu-id="bb11d-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-240">Obtiene el identificador de instancia de Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="bb11d-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="bb11d-242">8</span><span class="sxs-lookup"><span data-stu-id="bb11d-242">8</span></span> | <span data-ttu-id="bb11d-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-244">Obtiene el identificador de la ventana principal de Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="bb11d-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="bb11d-246">9</span><span class="sxs-lookup"><span data-stu-id="bb11d-246">9</span></span> | <span data-ttu-id="bb11d-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-248">Obtiene la ruta de acceso y el nombre del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="bb11d-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="bb11d-250">10</span><span class="sxs-lookup"><span data-stu-id="bb11d-250">10</span></span> | <span data-ttu-id="bb11d-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-252">Esta función está en desuso y ya no necesita que se llame.</span><span class="sxs-lookup"><span data-stu-id="bb11d-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="bb11d-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="bb11d-254">11</span><span class="sxs-lookup"><span data-stu-id="bb11d-254">11</span></span> | <span data-ttu-id="bb11d-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-256">Esta función está en desuso y ya no necesita que se llame.</span><span class="sxs-lookup"><span data-stu-id="bb11d-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="bb11d-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="bb11d-258">12</span><span class="sxs-lookup"><span data-stu-id="bb11d-258">12</span></span> | <span data-ttu-id="bb11d-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-260">Define un nombre binario de almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="bb11d-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="bb11d-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="bb11d-262">13</span><span class="sxs-lookup"><span data-stu-id="bb11d-262">13</span></span> | <span data-ttu-id="bb11d-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bb11d-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="bb11d-264">Obtiene los datos de un nombre almacenamiento persistente de binarios.</span><span class="sxs-lookup"><span data-stu-id="bb11d-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="bb11d-265">Devolver el valor XLOPER y XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="bb11d-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="bb11d-266">El argumento _operRes_ es el segundo argumento para las devoluciones de llamada y es un puntero a un **XLOPER** (**Excel4** y **Excel4v**) o **XLOPER12** (**Excel12** y **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="bb11d-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="bb11d-267">Después de una llamada correcta, que contiene el valor devuelto de la función o el comando.</span><span class="sxs-lookup"><span data-stu-id="bb11d-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="bb11d-268">**operRes** se puede establecer en cero (puntero nulo) si se requiere ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="bb11d-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="bb11d-269">Por lo que se debe liberar antes de cualquier memoria previamente que apunta a la llamada a fin de evitar pérdidas de memoria, se sobrescribe el contenido anterior de **operRes** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="bb11d-270">Si la función o el comando no se puede llamar (por ejemplo, si los argumentos no están correcta), **operRes** se establece en el error **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="bb11d-271">Un comando siempre devuelve **Boolean** **es TRUE** si es correcto, o **FALSE** si se produjo un error o el usuario cancelado.</span><span class="sxs-lookup"><span data-stu-id="bb11d-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="bb11d-272">Número de argumentos subsiguientes: count</span><span class="sxs-lookup"><span data-stu-id="bb11d-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="bb11d-273">El argumento _count_ es el tercer argumento para las devoluciones de llamada y es un entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bb11d-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="bb11d-274">Se debe establecer el número de argumentos subsiguientes, a partir de 1.</span><span class="sxs-lookup"><span data-stu-id="bb11d-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="bb11d-275">Si un comando o función no toma ningún argumento, se debe establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="bb11d-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="bb11d-276">En Microsoft Office Excel 2003, el número máximo de argumentos que puede realizar cualquier función es 30, aunque la mayoría toman menos de esto.</span><span class="sxs-lookup"><span data-stu-id="bb11d-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="bb11d-277">Iniciar en Excel 2007, el número máximo de argumentos que puede realizar cualquier función se ha aumentado a 255.</span><span class="sxs-lookup"><span data-stu-id="bb11d-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="bb11d-278">Con **Excel4** y **Excel12**, _count_ es el número de punteros a **XLOPER** o **XLOPER12** valores que se pasan.</span><span class="sxs-lookup"><span data-stu-id="bb11d-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="bb11d-279">Debe ser muy cuidado de no pase ese _recuento_ de menos argumentos que el valor se establece en.</span><span class="sxs-lookup"><span data-stu-id="bb11d-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="bb11d-280">Esto haría en Excel, leer con antelación a la pila e intenta procesar valores **XLOPER** o **XLOPER12** no válidos, lo que podrían provocar un bloqueo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb11d-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="bb11d-281">Con la **Excel4v** y **Excel12v**, _count_ es el tamaño de la matriz de punteros a **XLOPER** o **XLOPER12** valores que se pasa como el argumento final y siguiente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="bb11d-282">Una vez más, debe ser muy cuidado de no pasar una matriz más pequeña que el _recuento de_ elementos de tamaño, como los límites de la matriz que se va a saturación dará como resultado.</span><span class="sxs-lookup"><span data-stu-id="bb11d-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="bb11d-283">Pasar argumentos a funciones de la API de C</span><span class="sxs-lookup"><span data-stu-id="bb11d-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="bb11d-284">**Excel4** y **Excel12** tendrán longitud variable listas de argumentos, después de _recuento_, que se interpreta como punteros a valores **XLOPER** y **XLOPER12** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="bb11d-285">**Excel4v** y **Excel12v** toman un solo argumento, después de _recuento_, que es un puntero a una matriz de punteros a valores **XLOPER** en el caso de la **Excel4v**y a los valores de **XLOPER12** en el caso de **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="bb11d-286">Los formularios de matriz, la **Excel4v** y **Excel12v**, permiten una llamada a la API C de código de forma limpia cuando el número de argumentos es variable.</span><span class="sxs-lookup"><span data-stu-id="bb11d-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="bb11d-287">En el ejemplo siguiente se muestra una función que toma una matriz de tamaño variable de números y funciones de hoja de cálculo de Excel a través de la API de C, se utiliza para calcular la suma, promedio, mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="bb11d-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
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

<span data-ttu-id="bb11d-288">Reemplazar las referencias a valores **XLOPER12** con **XLOPER**y **Excel12v** con la **Excel4v**, en el código anterior diese como resultado una función que funcionaría con todas las versiones de Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="bb11d-289">Esta operación de las funciones de Excel **suma**, **promedio**, **MIN**y **MAX** es lo suficientemente simple para que sea más eficaz para ellos el código de C y para evitar la sobrecarga de preparación de los argumentos y la llamada a Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="bb11d-290">Sin embargo, muchas de las funciones de que Excel contiene son más complejos, hacer que este enfoque útil en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="bb11d-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="bb11d-291">El tema [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) proporciona otro ejemplo de trabajar con la **Excel4v** y **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-291">The [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="bb11d-292">Cuando se registra una función de hoja de cálculo XLL, puede proporcionar una cadena descriptiva para cada argumento que se usa en el cuadro de diálogo **Pegar función** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="bb11d-293">Por lo tanto, el número de argumentos totales que se proporciona para **xlfRegister** depende del número de argumentos que toma la función XLL y varían en función de una función a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="bb11d-294">Siempre se llama a una función de la API de C o un comando con el mismo número de argumentos, por lo que desea evitar el paso adicional de la creación de una matriz de punteros para esos argumentos.</span><span class="sxs-lookup"><span data-stu-id="bb11d-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="bb11d-295">En esos casos, es más sencillo y más ordenado para usar **Excel4** y **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="bb11d-296">Por ejemplo, cuando se registra los comandos y funciones XLL, debe proporcionar el nombre de archivo y ruta de acceso completo de la DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="bb11d-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="bb11d-297">Puede obtener el nombre de archivo en una llamada a **xlfGetName** y, a continuación, liberar con una llamada a **xlFree**, tal como se muestra en el siguiente ejemplo para **Excel4** y **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="bb11d-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
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

<span data-ttu-id="bb11d-298">En la práctica, la función, **Excel12v_example**, podría codificada de forma más eficaz mediante la creación de un único **xltypeMulti** **XLOPER12** argumento y llamar a la API C mediante el uso de **Excel12**, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb11d-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
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
> <span data-ttu-id="bb11d-299">En este caso, se omite el valor devuelto de **Excel12** .</span><span class="sxs-lookup"><span data-stu-id="bb11d-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="bb11d-300">En su lugar, el código comprueba que el devuelto **XLOPER12** es **xltypeNum** para determinar si la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="bb11d-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="bb11d-301">XLCallVer</span></span>

<span data-ttu-id="bb11d-302">Además de las devoluciones de llamada **Excel4**, **Excel4v**, **Excel12**y **Excel12v**, Excel exporta una función **XLCallVer**, que devuelve la versión de la API de C se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="bb11d-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="bb11d-303">El prototipo de función es como sigue:</span><span class="sxs-lookup"><span data-stu-id="bb11d-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="bb11d-304">Puede llamar a esta función, que es segura, desde cualquier comando XLL o función de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bb11d-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="bb11d-305">En Excel 97 a Excel 2003, **XLCallVer** devuelve 1280 = 0 x 0500 hex = 5 x 256, que indica la versión 5 de Excel.</span><span class="sxs-lookup"><span data-stu-id="bb11d-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="bb11d-306">Iniciar en Excel 2007, devuelve 0x0c00 = 3072 hex = 12 x 256, que indica la versión 12.</span><span class="sxs-lookup"><span data-stu-id="bb11d-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="bb11d-307">Aunque se puede usar para determinar si la nueva API de C está disponible en tiempo de ejecución, es posible que prefiera detectar la versión de Excel que se está ejecutando mediante el uso de `Excel4(xlfGetWorkspace, &version, 1, &arg)`, donde `arg` es un valor numérico **XLOPER** establecido en 2.</span><span class="sxs-lookup"><span data-stu-id="bb11d-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="bb11d-308">La función devuelve una cadena **XLOPER**, la versión, a continuación, se puede convertir a un número entero.</span><span class="sxs-lookup"><span data-stu-id="bb11d-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="bb11d-309">El motivo de la confianza en la versión de Excel en lugar de la versión de la API C es que no hay diferencias entre Excel 2000, Excel 2002 y Excel 2003 que el complemento es posible que también necesite detectar.</span><span class="sxs-lookup"><span data-stu-id="bb11d-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="bb11d-310">Por ejemplo, se realizaron cambios en la precisión de algunas de las funciones de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="bb11d-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb11d-311">Ver también</span><span class="sxs-lookup"><span data-stu-id="bb11d-311">See also</span></span>



[<span data-ttu-id="bb11d-312">Creación de XLL</span><span class="sxs-lookup"><span data-stu-id="bb11d-312">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="bb11d-313">Acceso al código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="bb11d-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="bb11d-314">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="bb11d-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
  
[<span data-ttu-id="bb11d-315">Devoluci�n de llamada de API de C funciona Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="bb11d-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
[<span data-ttu-id="bb11d-316">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="bb11d-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

