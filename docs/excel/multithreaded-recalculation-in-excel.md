---
title: Nuevo cálculo multiproceso en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- las celdas de seguros para subprocesos [excel 2007], subprocesamiento múltiple en Excel, tareas simultáneas [Excel 2007], funciones de seguros para subprocesos [Excel 2007], multiproceso recálculo [Excel 2007], MTR [Excel 2007], funciones XLL [Excel 2007], registrar como subprocesos, [recálculo Excel 2007], memoria multiproceso, contención [Excel 2007], registrar XLL funciona como subprocesos funciones no seguras de seguros [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815687"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="28a66-104">Nuevo cálculo multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="28a66-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28a66-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="28a66-106">Microsoft Office Excel 2007 fue la primera versión de Excel para usar el nuevo cálculo multiproceso (MTR) de hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="28a66-106">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets.</span></span> <span data-ttu-id="28a66-107">Puede configurar Excel para usar hasta subprocesos simultáneos 1024 al volver a calcular, independientemente del número de procesadores o núcleos de procesador en el equipo.</span><span class="sxs-lookup"><span data-stu-id="28a66-107">You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="28a66-108">No hay un sistema operativo sobrecarga asociado con cada subproceso, por lo que no debe configurar Excel para usar más subprocesos de los que necesita.</span><span class="sxs-lookup"><span data-stu-id="28a66-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="28a66-109">Si el equipo tiene varios procesadores o núcleos de procesador, el sistema operativo tiene responsabilidad de asignación de los subprocesos a los procesadores de la manera más eficaz.</span><span class="sxs-lookup"><span data-stu-id="28a66-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="28a66-110">Introducción a Excel MTR</span><span class="sxs-lookup"><span data-stu-id="28a66-110">Excel MTR overview</span></span>

<span data-ttu-id="28a66-111">Excel intenta identificar las partes de la cadena de cálculo que se pueden volver a calcularse simultáneamente en distintos subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-111">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads.</span></span> <span data-ttu-id="28a66-112">El siguiente árbol muy simple (donde x ← y significa y sólo depende de x), muestra un ejemplo de esto.</span><span class="sxs-lookup"><span data-stu-id="28a66-112">The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="28a66-113">**En la figura 1. Cálculo simultáneo en distintos subprocesos**</span><span class="sxs-lookup"><span data-stu-id="28a66-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="28a66-114">![Cálculo simultáneo en distintos subprocesos] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultáneo en distintos subprocesos")</span><span class="sxs-lookup"><span data-stu-id="28a66-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="28a66-115">Una vez que se calcula A1, A2 y, a continuación, A3 se pueden calcular en un subproceso mientras B1 y, a continuación, C1 se pueden calcular en otro, suponiendo que todas las celdas son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="28a66-116">La celda de seguros para subprocesos términos significa una celda que contiene sólo las funciones de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-116">The term thread-safe cell means a cell that only contains thread-safe functions.</span></span> <span data-ttu-id="28a66-117">¿Qué es y no es segura para subprocesos se detallan [es no considera subproceso seguros por Excel y ¿qué es](#xl2007xllsdk_threadsafe).</span><span class="sxs-lookup"><span data-stu-id="28a66-117">What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="28a66-118">Los libros más prácticos contienen árboles de dependencia mucho más complejos que en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="28a66-118">Most practical workbooks contain far more complex dependency trees than this example.</span></span> <span data-ttu-id="28a66-119">Además, no se puede conocer la hora de actualización de una celda hasta que se realiza un cálculo y se puede variar mucho dependiendo de los argumentos de las funciones.</span><span class="sxs-lookup"><span data-stu-id="28a66-119">Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments.</span></span> <span data-ttu-id="28a66-120">Para obtener los mejores resultados, Excel intenta mejorar el orden de cálculo en todos los cálculos hasta que es posible mejorar la optimización.</span><span class="sxs-lookup"><span data-stu-id="28a66-120">To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="28a66-121">Excel utiliza un único subproceso principal para ejecutar o ejecutar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28a66-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="28a66-122">Comandos integrados</span><span class="sxs-lookup"><span data-stu-id="28a66-122">Built-in commands</span></span>
    
- <span data-ttu-id="28a66-123">Comandos XLL</span><span class="sxs-lookup"><span data-stu-id="28a66-123">XLL commands</span></span>
    
- <span data-ttu-id="28a66-124">Funciones de interfaz de administrador de complementos XLL (función**xlAutoOpen** y así sucesivamente)</span><span class="sxs-lookup"><span data-stu-id="28a66-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="28a66-125">Microsoft Visual Basic para aplicaciones (VBA) definidas por el usuario los comandos (que suele denominados macros)</span><span class="sxs-lookup"><span data-stu-id="28a66-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="28a66-126">Funciones definidas por el usuario VBA</span><span class="sxs-lookup"><span data-stu-id="28a66-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="28a66-127">Funciones integradas de hoja de cálculo no seguras subproceso (vea la sección siguiente para obtener una lista)</span><span class="sxs-lookup"><span data-stu-id="28a66-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="28a66-128">Funciones y comandos definidas por el usuario de la hoja de macros XLM</span><span class="sxs-lookup"><span data-stu-id="28a66-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="28a66-129">Funciones y comandos de complementos COM</span><span class="sxs-lookup"><span data-stu-id="28a66-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="28a66-130">Funciones y operadores dentro de las expresiones de formato condicionales</span><span class="sxs-lookup"><span data-stu-id="28a66-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="28a66-131">Funciones y operadores dentro de las definiciones de nombre definido que se utiliza en las fórmulas de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="28a66-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="28a66-132">La evaluación de una expresión en el cuadro Editar fórmula con la tecla **F9** forzada</span><span class="sxs-lookup"><span data-stu-id="28a66-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="28a66-133">Todas las fórmulas de hoja de cálculo, independientemente de si las funciones son seguros para subprocesos o no, se evalúan en el subproceso principal a menos que Excel está configurado para usar más de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-133">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread.</span></span> <span data-ttu-id="28a66-134">Cuando el usuario especifica que se debe usar más de un subproceso, los subprocesos adicionales se utilizan para las celdas de seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-134">When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells.</span></span> <span data-ttu-id="28a66-135">Tenga en cuenta que el subproceso principal aún se puede usar para las celdas de seguros para subprocesos cuando tenga sentido desde el punto de equilibrio de carga de vista.</span><span class="sxs-lookup"><span data-stu-id="28a66-135">Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="28a66-136">Merece la pena reformular que Excel no ejecute más de un comando a la vez, por lo que no es necesario emplear las mismas precauciones como cuando se escriben funciones de seguros para subprocesos, como el uso de memoria de proceso local y secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="28a66-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="28a66-137">¿Qué es y no se considera subproceso seguros por Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="28a66-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="28a66-138"></span></span>

<span data-ttu-id="28a66-139">Excel sólo tiene en cuenta lo siguiente como subproceso seguro:</span><span class="sxs-lookup"><span data-stu-id="28a66-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="28a66-140">Todos los operadores unario y binario de Excel.</span><span class="sxs-lookup"><span data-stu-id="28a66-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="28a66-141">Casi todas las funciones de hoja de cálculo integradas a partir de Excel 2007 (vea la lista de excepciones)</span><span class="sxs-lookup"><span data-stu-id="28a66-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="28a66-142">En Agregar funciones XLL que se han registrado explícitamente como seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="28a66-143">Las funciones de hoja de cálculo integradas que no son seguros para subprocesos son:</span><span class="sxs-lookup"><span data-stu-id="28a66-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="28a66-144">**FONÉTICO**</span><span class="sxs-lookup"><span data-stu-id="28a66-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="28a66-145">**Celda** cuando se utiliza el "formato de" o la "dirección" argumento</span><span class="sxs-lookup"><span data-stu-id="28a66-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="28a66-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="28a66-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="28a66-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="28a66-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="28a66-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="28a66-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="28a66-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="28a66-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="28a66-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="28a66-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="28a66-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="28a66-151">**CUBESET**</span></span>
    
- <span data-ttu-id="28a66-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="28a66-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="28a66-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="28a66-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="28a66-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="28a66-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="28a66-155">**Dirección** donde se proporciona el quinto parámetro (sheet_name)</span><span class="sxs-lookup"><span data-stu-id="28a66-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="28a66-156">Cualquier función de base de datos (**DSUM**, **DAVERAGE**etc.) que hace referencia a una tabla dinámica</span><span class="sxs-lookup"><span data-stu-id="28a66-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="28a66-157">**ERROR. TIPO DE**</span><span class="sxs-lookup"><span data-stu-id="28a66-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="28a66-158">**HIPERVÍNCULO**</span><span class="sxs-lookup"><span data-stu-id="28a66-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="28a66-159">Para que sea explícito, las siguientes se consideran no seguras:</span><span class="sxs-lookup"><span data-stu-id="28a66-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="28a66-160">Funciones definidas por el usuario VBA</span><span class="sxs-lookup"><span data-stu-id="28a66-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="28a66-161">Complemento definidas por el usuario funciones COM</span><span class="sxs-lookup"><span data-stu-id="28a66-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="28a66-162">Funciones definidas por el usuario de hoja de macros XLM</span><span class="sxs-lookup"><span data-stu-id="28a66-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="28a66-163">Funciones de complementos XLL registran no explícitamente como seguros para subprocesos</span><span class="sxs-lookup"><span data-stu-id="28a66-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="28a66-164">Las implicaciones son que las siguientes operaciones y funciones no son seguros para subprocesos y producirá un error si se les llama desde una función XLL registrada como seguros para subprocesos:</span><span class="sxs-lookup"><span data-stu-id="28a66-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="28a66-165">Llama a las funciones de información XLM, por ejemplo, **xlfGetCell** (**GET. CELDA**).</span><span class="sxs-lookup"><span data-stu-id="28a66-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="28a66-166">Llama a **xlfSetName** (**SET.NAME**) para definir o eliminar nombres internos de XLL.</span><span class="sxs-lookup"><span data-stu-id="28a66-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="28a66-167">Llamadas a funciones no seguras subproceso definidas por el usuario mediante **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="28a66-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="28a66-168">Llama a la función [xlfEvaluate](xlfevaluate.md) para expresiones que contienen funciones no seguras subproceso o que contienen nombres definidos cuyas definiciones contienen funciones no seguras subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="28a66-169">Llamadas a la función [xlAbort](xlabort.md) para borrar una condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="28a66-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="28a66-170">Llamadas a la función [xlCoerce](xlcoerce.md) para obtener el valor de una referencia de celda no calculada.</span><span class="sxs-lookup"><span data-stu-id="28a66-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="28a66-171">No se permiten las funciones de hoja de cálculo XLL para llamar a los comandos de la API de C, por ejemplo, **xlcSave**, independientemente de si se han registrado como seguros para subprocesos o no.</span><span class="sxs-lookup"><span data-stu-id="28a66-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="28a66-172">Dado que las funciones XLL declaran como seguros para subprocesos no se puede llamar a las funciones de información XLM o referencia a celdas sin calcular, Excel no permite funciones XLL que se registran como equivalentes de hojas de macro también debe registrarse como seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-172">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe.</span></span> <span data-ttu-id="28a66-173">Por lo tanto, si se intenta obtener el valor de una referencia de celda no calculada mediante **xlCoerce** produce el error **xlretUncalced** .</span><span class="sxs-lookup"><span data-stu-id="28a66-173">Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error.</span></span> <span data-ttu-id="28a66-174">Llamar a un XLM función de la información se produce un error con un error **xlretFailed** .</span><span class="sxs-lookup"><span data-stu-id="28a66-174">Calling an XLM information function fails with an **xlretFailed** error.</span></span> <span data-ttu-id="28a66-175">Los otros puntos enumerados anteriormente producirá un error con un código de error que se introdujo en la API de C de Excel: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="28a66-175">The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="28a66-176">Las funciones de devolución de llamada sólo API de C son seguros para todos los subprocesos:</span><span class="sxs-lookup"><span data-stu-id="28a66-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="28a66-177">**xlCoerce** (excepto aunque coerción de celda no calculada hace referencia se produce un error)</span><span class="sxs-lookup"><span data-stu-id="28a66-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="28a66-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="28a66-178">**xlFree**</span></span>
    
- <span data-ttu-id="28a66-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="28a66-179">**xlStack**</span></span>
    
- <span data-ttu-id="28a66-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="28a66-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="28a66-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="28a66-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="28a66-182">**xlAbort** (excepto cuando se utiliza para borrar una condición de interrupción)</span><span class="sxs-lookup"><span data-stu-id="28a66-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="28a66-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="28a66-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="28a66-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="28a66-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="28a66-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="28a66-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="28a66-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="28a66-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="28a66-187">La única excepción es la función **xlSet** , que es, en cualquier caso, un equivalente de comando y por lo tanto no se puede llamar desde ninguna función de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="28a66-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="28a66-188">Una función de hoja de cálculo XLL puede estar registrada con Excel como seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-188">An XLL worksheet function can be registered with Excel as thread safe.</span></span> <span data-ttu-id="28a66-189">Esto indica a Excel que la función se puede llamar de forma segura y simultáneamente en varios subprocesos, si bien, debe asegurarse de que éste es realmente el caso.</span><span class="sxs-lookup"><span data-stu-id="28a66-189">This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case.</span></span> <span data-ttu-id="28a66-190">Posiblemente puede desestabilizar Excel si una función registrada como seguros para subprocesos, a continuación, se comporta de forma no segura.</span><span class="sxs-lookup"><span data-stu-id="28a66-190">You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="28a66-191">Registrar funciones XLL como seguros para subprocesos</span><span class="sxs-lookup"><span data-stu-id="28a66-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="28a66-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="28a66-192"></span></span>

<span data-ttu-id="28a66-193">Las reglas que un programador debe cumplir al escribir funciones de subprocesos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="28a66-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="28a66-194">No llame a recursos de otras DLL que puede no ser seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="28a66-195">No realice las llamadas no seguras subproceso a través de la API de C o COM.</span><span class="sxs-lookup"><span data-stu-id="28a66-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="28a66-196">Proteger los recursos que podrían utilizarse simultáneamente por más de un subproceso mediante secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="28a66-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="28a66-197">Utilizar memoria local de subprocesos para el almacenamiento de específicas de un subproceso y sustituir las variables estáticas dentro de las funciones con variables locales de subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="28a66-198">Excel impone una restricción adicional: funciones de subprocesos no se puede registrar como equivalentes de la hoja de macros y por lo tanto, no se pueden llamar a las funciones de información XLM u obtener los valores de celdas no vuelve a calcular.</span><span class="sxs-lookup"><span data-stu-id="28a66-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="28a66-199">Contención de memoria</span><span class="sxs-lookup"><span data-stu-id="28a66-199">Memory contention</span></span>
<span data-ttu-id="28a66-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="28a66-200"></span></span>

<span data-ttu-id="28a66-201">Sistemas multiproceso deben solucionar dos problemas fundamentales:</span><span class="sxs-lookup"><span data-stu-id="28a66-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="28a66-202">Procedimiento para proteger la memoria que debe ser leen o escriben en, por más de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="28a66-203">Procedimiento para crear y obtener acceso a memoria que está asociado con y, a continuación, por lo que privada al subproceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="28a66-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="28a66-204">El sistema operativo Windows y el Kit de desarrollo de Software (SDK) de Windows proporcionan herramientas para estos dos: las secciones críticas y la API de almacenamiento local de subprocesos (TLS) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="28a66-204">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively.</span></span> <span data-ttu-id="28a66-205">Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="28a66-205">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="28a66-206">Por ejemplo, el primer problema puede surgir cuando dos funciones de hoja de cálculo (o dos instancias de la misma función simultáneamente ejecución) necesitan tener acceso o modificar una variable global en un proyecto de DLL.</span><span class="sxs-lookup"><span data-stu-id="28a66-206">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project.</span></span> <span data-ttu-id="28a66-207">Recuerde que este tipo de variable global podría estar oculto en una instancia de un objeto de clase globalmente accesible.</span><span class="sxs-lookup"><span data-stu-id="28a66-207">Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="28a66-208">El segundo problema puede surgir, por ejemplo, cuando una función de hoja de cálculo que declara una variable estática o un objeto dentro del código del cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="28a66-208">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code.</span></span> <span data-ttu-id="28a66-209">El compilador de C o C++ sólo crea una única copia que usan todos los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-209">The C/C++ compiler only creates a single copy that all threads use.</span></span> <span data-ttu-id="28a66-210">Esto significa que una instancia de la función puede cambiar el valor, mientras que otra en un subproceso diferente podría ser suponiendo que el valor es qué lo establecido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="28a66-210">This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="28a66-211">Aplicaciones de ejemplo de MTR</span><span class="sxs-lookup"><span data-stu-id="28a66-211">Example applications of MTR</span></span>
<span data-ttu-id="28a66-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="28a66-212"></span></span>

<span data-ttu-id="28a66-213">Cualquier XLL que exporta las funciones de hoja de cálculo puede aprovechar la actualización del cálculo multiproceso (MTR) en Excel siempre que dichas funciones no es necesario llevar a cabo acciones no seguras subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-213">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions.</span></span> <span data-ttu-id="28a66-214">Esto permite que Excel para volver a calcular libros que dependen de ellos tan pronto como sea posible y es, por tanto, lo deseable que la aplicación.</span><span class="sxs-lookup"><span data-stu-id="28a66-214">This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="28a66-215">En concreto, MTR tiene un impacto enorme en el tiempo de actualización de los libros que llaman a funciones definidas por el usuario (UDF) que ellos mismos llamar a procesos externos para obtener el resultado deseado.</span><span class="sxs-lookup"><span data-stu-id="28a66-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="28a66-216">En concreto, considere la posibilidad de una UDF que llame a un servidor remoto que puede procesar simultáneamente muchas solicitudes y un libro que contiene todas las llamadas a esa función.</span><span class="sxs-lookup"><span data-stu-id="28a66-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="28a66-217">Si recálculo del libro tiene un único subproceso, cada uno de ellos llamar a las UDF y, por lo que en el servidor remoto, debe completar antes de hacer lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="28a66-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="28a66-218">Se pierde la capacidad del servidor para procesar todas las llamadas a la vez.</span><span class="sxs-lookup"><span data-stu-id="28a66-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="28a66-219">Si el nuevo cálculo del libro es multiproceso, Excel puede realizar varias llamadas al mismo tiempo o en una sucesión rápida.</span><span class="sxs-lookup"><span data-stu-id="28a66-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="28a66-220">Si Excel está configurada para usar el mismo número de subprocesos que el servidor: llamar N — y la topología del árbol de la dependencia del libro lo permita, se podría reducir el tiempo total para algo alcanzando 1/N del tiempo de cálculo de un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-220">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time.</span></span> <span data-ttu-id="28a66-221">Esto puede ser cierto incluso cuando el equipo cliente (en el que el libro se está ejecutando) sólo tiene un procesador, especialmente donde el tiempo necesario para realizar la llamada al servidor es pequeño en relación con el tiempo que tarda el servidor en proceso de la llamada.</span><span class="sxs-lookup"><span data-stu-id="28a66-221">This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="28a66-222">Hay sobrecarga de sistema operativo para cada subproceso adicional.</span><span class="sxs-lookup"><span data-stu-id="28a66-222">There is operating system overhead for each additional thread.</span></span> <span data-ttu-id="28a66-223">Por lo tanto, es posible que algunos experimentación necesario para un libro determinado y un servidor determinado y el equipo cliente para encontrar el número óptimo de subprocesos de que Excel se debe indicar a usar.</span><span class="sxs-lookup"><span data-stu-id="28a66-223">Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="28a66-224">Por ejemplo, considere la posibilidad de un equipo de procesador único que ejecuta Excel y un libro que contiene las celdas de 1.000.</span><span class="sxs-lookup"><span data-stu-id="28a66-224">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells.</span></span> <span data-ttu-id="28a66-225">Se llama a UDF, que llama a su vez uno o varios servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="28a66-225">It calls a UDF, which in turn calls one or more remote servers.</span></span> <span data-ttu-id="28a66-226">Se supone que las 1.000 celdas no dependen de la otra, por lo que Excel no hay que esperar a una llamada para llevar a cabo antes de llamar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="28a66-226">Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next.</span></span> <span data-ttu-id="28a66-227">(Algunas descanso de esta restricción es posible sin que ello afecte en este ejemplo). Si los servidores pueden procesar las solicitudes de 100 simultáneamente, y Excel está configurado para usar 100 subprocesos, se pueden reducir el tiempo de ejecución con tan sólo 1/100 de ese where sólo un subproceso que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="28a66-227">(Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used.</span></span> <span data-ttu-id="28a66-228">La sobrecarga es decir asociados con Excel asignación de llamadas para cada subproceso y el sistema operativo de administración de 100 subprocesos significa que, en la práctica, la reducción no será un proceso bastante este excelente.</span><span class="sxs-lookup"><span data-stu-id="28a66-228">The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great.</span></span> <span data-ttu-id="28a66-229">También hay una suposición implícita aquí que el servidor funciona bien y solicitando que procesar 100 tareas simultáneamente no afectará a los tiempos de finalización de tareas individuales considerablemente.</span><span class="sxs-lookup"><span data-stu-id="28a66-229">There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="28a66-230">Una aplicación práctica en la que esta técnica puede tener una ventaja importante es de métodos de Monte Carlo, así como otras tareas numéricamente intensivos que se pueden dividir en las subtareas más pequeñas que pueden se puede asignar a los servidores.</span><span class="sxs-lookup"><span data-stu-id="28a66-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="28a66-231">Consideraciones sobre servicios de Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-231">Excel Services considerations</span></span>
<span data-ttu-id="28a66-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="28a66-232"></span></span>

<span data-ttu-id="28a66-233">Excel Services admite la carga, calcular y la representación de hojas de cálculo de Excel en un servidor.</span><span class="sxs-lookup"><span data-stu-id="28a66-233">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server.</span></span> <span data-ttu-id="28a66-234">Los usuarios pueden, a continuación, obtener acceso e interactuar con las hojas de cálculo mediante el uso de herramientas de explorador estándar.</span><span class="sxs-lookup"><span data-stu-id="28a66-234">Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="28a66-235">UDF de Excel Services se crean mediante código administrado de Microsoft .NET Framework y disponible aunque un ensamblado. NET.</span><span class="sxs-lookup"><span data-stu-id="28a66-235">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly.</span></span> <span data-ttu-id="28a66-236">No se admiten los XLL de Excel Services.</span><span class="sxs-lookup"><span data-stu-id="28a66-236">XLLs are not supported by Excel Services.</span></span> <span data-ttu-id="28a66-237">Un servidor recursos UDF de código administrado puede llamar a un XLL para tener acceso a su funcionalidad, por lo que el usuario puede tener la misma funcionalidad con un libro cargado en servidor al igual que con un libro cargado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="28a66-237">A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="28a66-238">Para disponer de las funciones de los XLL de esta manera, que por lo tanto, se deben ajustan en un ensamblado de .NET para los tipos de datos administrados de .NET Framework que convierte los argumentos y valores devueltos de los tipos de datos nativos y que llama a las funciones XLL.</span><span class="sxs-lookup"><span data-stu-id="28a66-238">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions.</span></span> <span data-ttu-id="28a66-239">El contenedor de .NET exportará un UDF de servidor para cada función XLL que se tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="28a66-239">The .NET wrapper would export one server UDF for each XLL function being accessed.</span></span> <span data-ttu-id="28a66-240">Un requisito adicional es que las funciones XLL llamadas de esta forma deben ser seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-240">An additional requirement is that any XLL functions called in this way must be thread safe.</span></span> <span data-ttu-id="28a66-241">Debido a que las funciones XLL no están registradas en el modo en que son con el cliente de Excel, el servidor y el contenedor de .NET no tienen ninguna manera de exigir que son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="28a66-241">Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe.</span></span> <span data-ttu-id="28a66-242">Es responsabilidad del desarrollador XLL para asegurarse de esto.</span><span class="sxs-lookup"><span data-stu-id="28a66-242">It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28a66-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="28a66-243">See also</span></span>

- [<span data-ttu-id="28a66-244">Actualización de Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="28a66-245">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="28a66-246">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="28a66-247">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="28a66-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="28a66-248">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="28a66-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

