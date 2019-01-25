---
title: Actualización multiproceso en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- celdas seguras para subprocesos [excel 2007],multithreading en Excel,tareas simultáneas [Excel 2007],funciones seguras para subprocesos [Excel 2007],actualización multiproceso [Excel 2007],MTR [Excel 2007],funciones XLL [Excel 2007], registrar como seguro para subprocesos,actualización [Excel 2007], multiproceso,contención de memoria [Excel 2007],registrar funciones XLL como seguras para subprocesos [Excel 2007],funciones no seguras [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720712"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="948ec-104">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="948ec-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="948ec-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="948ec-106">Microsoft Office Excel 2007 fue la primera versión de Excel en usar la actualización multiproceso (MTR) de hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="948ec-106">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets.</span></span> <span data-ttu-id="948ec-107">Puede configurar Excel para usar hasta 1024 subprocesos simultáneos al actualizar, independientemente del número de procesadores o núcleos de procesador en el equipo.</span><span class="sxs-lookup"><span data-stu-id="948ec-107">You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="948ec-108">Hay una sobrecarga del sistema operativo asociada a cada subproceso, por lo que no debe configurar Excel para usar más subprocesos de los que necesita.</span><span class="sxs-lookup"><span data-stu-id="948ec-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="948ec-109">Si el equipo tiene varios procesadores o núcleos de procesador, el sistema operativo asume la responsabilidad de asignar los subprocesos a los procesadores de la manera más eficiente.</span><span class="sxs-lookup"><span data-stu-id="948ec-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="948ec-110">Información general sobre MTR en Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-110">Excel MTR overview</span></span>

<span data-ttu-id="948ec-111">Excel intenta identificar partes de la cadena de cálculo que se pueden actualizar simultáneamente en subprocesos distintos.</span><span class="sxs-lookup"><span data-stu-id="948ec-111">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads.</span></span> <span data-ttu-id="948ec-112">El siguiente árbol muy sencillo (donde x ← y significa y solo depende de x) muestra un ejemplo de ello.</span><span class="sxs-lookup"><span data-stu-id="948ec-112">The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="948ec-113">**Figura 1. Cálculo simultáneo en subprocesos distintos**</span><span class="sxs-lookup"><span data-stu-id="948ec-113">**Calculating concurrently on different threads**</span></span>

<span data-ttu-id="948ec-114">![Cálculo simultáneo en subprocesos distintos](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultáneo en subprocesos distintos")</span><span class="sxs-lookup"><span data-stu-id="948ec-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="948ec-115">Después de calcular A1, A2 y A3 pueden calcularse en un subproceso, mientras que B1 y C1 se pueden calcular en otro, suponiendo que todas las celdas son seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="948ec-116">El término “celda segura para subprocesos” se refiere a una celda que solo contiene funciones seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-116">The term thread-safe cell means a cell that only contains thread-safe functions.</span></span> <span data-ttu-id="948ec-117">Consulte la sección [Qué se considera y qué no se considera seguro para subprocesos en Excel](#xl2007xllsdk_threadsafe) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="948ec-117">What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="948ec-118">Los libros más prácticos contienen árboles de dependencias mucho más complejos que este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="948ec-118">Most practical workbooks contain far more complex dependency trees than this example.</span></span> <span data-ttu-id="948ec-119">Además, el tiempo de actualización de una celda no se puede conocer hasta que el cálculo ha finalizado y puede variar enormemente según los argumentos de las funciones.</span><span class="sxs-lookup"><span data-stu-id="948ec-119">Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments.</span></span> <span data-ttu-id="948ec-120">Para obtener los mejores resultados, Excel intenta mejorar el orden de cálculo en cada cálculo hasta que es posible mejorar la optimización.</span><span class="sxs-lookup"><span data-stu-id="948ec-120">To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="948ec-121">Excel usa un solo subproceso principal para ejecutar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="948ec-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="948ec-122">Comandos integrados</span><span class="sxs-lookup"><span data-stu-id="948ec-122">Built-in commands</span></span>
    
- <span data-ttu-id="948ec-123">Comandos XLL</span><span class="sxs-lookup"><span data-stu-id="948ec-123">XLL commands</span></span>
    
- <span data-ttu-id="948ec-124">Funciones de interfaz del Administrador de complementos XLL (función **xlAutoOpen**, etc.)</span><span class="sxs-lookup"><span data-stu-id="948ec-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="948ec-125">Comandos definidos por el usuario de Microsoft Visual Basic para Aplicaciones (VBA) (a menudo denominadas macros)</span><span class="sxs-lookup"><span data-stu-id="948ec-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="948ec-126">Funciones definidas por el usuario de VBA</span><span class="sxs-lookup"><span data-stu-id="948ec-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="948ec-127">Funciones integradas de hoja de cálculo no segura para subprocesos (consulte la siguiente sección para obtener una lista)</span><span class="sxs-lookup"><span data-stu-id="948ec-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="948ec-128">Funciones y comandos definidos por el usuario de la hoja de macros XLM</span><span class="sxs-lookup"><span data-stu-id="948ec-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="948ec-129">Funciones y comandos de complemento COM</span><span class="sxs-lookup"><span data-stu-id="948ec-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="948ec-130">Funciones y operadores dentro de las expresiones de formato condicional</span><span class="sxs-lookup"><span data-stu-id="948ec-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="948ec-131">Funciones y operadores dentro de las definiciones de nombre definido que se usan en las fórmulas de hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="948ec-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="948ec-132">La evaluación de una expresión en el cuadro de edición de la fórmula con la tecla **F9**</span><span class="sxs-lookup"><span data-stu-id="948ec-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="948ec-133">Todas las fórmulas de hoja de cálculo, independientemente de si las funciones son seguras para subprocesos o no, se evalúan en el subproceso principal a menos que Excel esté configurado para usar más de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="948ec-133">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread.</span></span> <span data-ttu-id="948ec-134">Cuando el usuario especifica que debe usarse más de un subproceso, los subprocesos adicionales se usan para las celdas seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-134">When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells.</span></span> <span data-ttu-id="948ec-135">Tenga en cuenta que el subproceso principal aún puede usarse para las celdas seguras para subprocesos cuando tiene sentido desde un punto de vista de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="948ec-135">Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="948ec-136">Conviene reformular que Excel no ejecuta más de un comando a la vez, por lo que no es necesario usar las mismas precauciones que cuando se escriben funciones seguras para subprocesos, como el uso de memoria local para el subproceso y secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="948ec-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="948ec-137">Qué se considera y qué no se considera seguro para subprocesos en Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="948ec-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="948ec-138"></span></span>

<span data-ttu-id="948ec-139">En Excel solo se considera seguro para subprocesos lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="948ec-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="948ec-140">Todos los operadores unarios y binarios en Excel.</span><span class="sxs-lookup"><span data-stu-id="948ec-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="948ec-141">Casi todas las funciones de hoja de cálculo integradas a partir de Excel 2007 (vea la lista de excepciones)</span><span class="sxs-lookup"><span data-stu-id="948ec-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="948ec-142">Funciones de complemento XLL que se han registrado explícitamente como seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="948ec-143">Las funciones de hoja de cálculo integradas que no son seguras para subprocesos son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="948ec-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="948ec-144">**PHONETIC**</span><span class="sxs-lookup"><span data-stu-id="948ec-144">**Phonetic**</span></span>
    
- <span data-ttu-id="948ec-145">**CELL** cuando se usa el argumento "format" o "address"</span><span class="sxs-lookup"><span data-stu-id="948ec-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="948ec-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="948ec-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="948ec-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="948ec-147">**GetPivotData**</span></span>
    
- <span data-ttu-id="948ec-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="948ec-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="948ec-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="948ec-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="948ec-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="948ec-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="948ec-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="948ec-151">**CUBESET**</span></span>
    
- <span data-ttu-id="948ec-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="948ec-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="948ec-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="948ec-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="948ec-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="948ec-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="948ec-155">**ADDRESS** donde se proporciona el quinto parámetro (sheet_name)</span><span class="sxs-lookup"><span data-stu-id="948ec-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="948ec-156">Ninguna función de base de datos (**BDSUMA**, **BDPROMEDIO**, etc.) que haga referencia a una tabla dinámica</span><span class="sxs-lookup"><span data-stu-id="948ec-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="948ec-157">**ERROR.TYPE**</span><span class="sxs-lookup"><span data-stu-id="948ec-157">**ErrorType**</span></span>
    
- <span data-ttu-id="948ec-158">**HYPERLINK**</span><span class="sxs-lookup"><span data-stu-id="948ec-158">**hyperlink**</span></span>
    
<span data-ttu-id="948ec-159">Para ser explícitos, lo siguiente se considera como no seguro:</span><span class="sxs-lookup"><span data-stu-id="948ec-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="948ec-160">Funciones definidas por el usuario de VBA</span><span class="sxs-lookup"><span data-stu-id="948ec-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="948ec-161">Funciones definidas por el usuario de complemento COM</span><span class="sxs-lookup"><span data-stu-id="948ec-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="948ec-162">Funciones definidas por el usuario de hoja de macros XLM</span><span class="sxs-lookup"><span data-stu-id="948ec-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="948ec-163">Funciones de complemento XLL que se han registrado explícitamente como seguras para subprocesos</span><span class="sxs-lookup"><span data-stu-id="948ec-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="948ec-164">Las consecuencias son que las siguientes operaciones y funciones no son seguras para subprocesos y producen un error si se les llama desde una función XLL registrada como segura para subprocesos:</span><span class="sxs-lookup"><span data-stu-id="948ec-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="948ec-165">Llamadas a funciones de información XLM, por ejemplo, **xlfGetCell** (**GET.CELL**).</span><span class="sxs-lookup"><span data-stu-id="948ec-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="948ec-166">Llamadas a **xlfSetName** (**SET.NAME**) para definir o eliminar nombres internos de XLL.</span><span class="sxs-lookup"><span data-stu-id="948ec-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="948ec-167">Llamadas a funciones definidas por el usuario no seguras para subprocesos con **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="948ec-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="948ec-168">Llamadas a la función [xlfEvaluate](xlfevaluate.md) para expresiones que contienen funciones no seguras para subprocesos o que contienen nombres definidos cuyas definiciones contienen funciones no seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="948ec-169">Llamadas a la función [xlAbort](xlabort.md) para borrar una condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="948ec-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="948ec-170">Llamadas a la función [xlCoerce](xlcoerce.md) para obtener el valor de una referencia de celda no actualizada.</span><span class="sxs-lookup"><span data-stu-id="948ec-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="948ec-171">Las funciones de hoja de cálculo XLL no están permitidas para llamar a los comandos de la API de C, por ejemplo, **xlcSave**, independientemente de si se han registrado como seguras para subprocesos o no.</span><span class="sxs-lookup"><span data-stu-id="948ec-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="948ec-172">Dado que las funciones XLL declaradas como seguras para subprocesos no pueden llamar a las funciones de información XLM o hacer referencia a las celdas no actualizadas, Excel no permite que las funciones XLL registrados como equivalentes de hojas de macros se registren también como seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-172">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe.</span></span> <span data-ttu-id="948ec-173">Por tanto, al intentar obtener el valor de una referencia de celda no actualizada mediante **xlCoerce** se produce el error **xlretUncalced**.</span><span class="sxs-lookup"><span data-stu-id="948ec-173">Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error.</span></span> <span data-ttu-id="948ec-174">Una llamada a una función de información XLM produce un error **xlretFailed**.</span><span class="sxs-lookup"><span data-stu-id="948ec-174">Calling an XLM information function fails with an **xlretFailed** error.</span></span> <span data-ttu-id="948ec-175">Los otros puntos enumerados anteriormente producen un error con un código introducido en la API de C de Excel: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="948ec-175">The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="948ec-176">Todas las funciones de devolución de llamada solo para API de C son seguras para subprocesos:</span><span class="sxs-lookup"><span data-stu-id="948ec-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="948ec-177">**xlCoerce** (excepto cuando haya un error en la coerción de las referencias de celda no actualizadas)</span><span class="sxs-lookup"><span data-stu-id="948ec-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="948ec-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="948ec-178">**xlFree**</span></span>
    
- <span data-ttu-id="948ec-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="948ec-179">**xlStack**</span></span>
    
- <span data-ttu-id="948ec-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="948ec-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="948ec-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="948ec-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="948ec-182">**xlAbort** (excepto cuando se usa para borrar una condición de interrupción)</span><span class="sxs-lookup"><span data-stu-id="948ec-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="948ec-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="948ec-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="948ec-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="948ec-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="948ec-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="948ec-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="948ec-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="948ec-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="948ec-187">La única excepción es la función **xlSet**, que es, en todo caso, equivalente a un comando y no puede llamarse desde ninguna función de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="948ec-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="948ec-188">Una función de hoja de cálculo XLL se puede registrar con Excel como segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-188">An XLL worksheet function can be registered with Excel as thread safe.</span></span> <span data-ttu-id="948ec-189">Esto indica a Excel que la función puede llamarse de forma segura y simultáneamente en varios subprocesos, aunque debe asegurarse de que realmente es así.</span><span class="sxs-lookup"><span data-stu-id="948ec-189">This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case.</span></span> <span data-ttu-id="948ec-190">Si una función registrada como segura para subprocesos se comporta de forma no segura, probablemente podría desestabilizar Excel.</span><span class="sxs-lookup"><span data-stu-id="948ec-190">You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="948ec-191">Registrar funciones XLL como seguras para subprocesos</span><span class="sxs-lookup"><span data-stu-id="948ec-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="948ec-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="948ec-192"></span></span>

<span data-ttu-id="948ec-193">Un desarrollador debe cumplir las siguientes reglas al escribir funciones seguras para subprocesos:</span><span class="sxs-lookup"><span data-stu-id="948ec-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="948ec-194">No llamar a recursos de otras DLL que posiblemente no sean seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="948ec-195">No realizar ninguna llamada no segura para subprocesos a través de la API de C o COM.</span><span class="sxs-lookup"><span data-stu-id="948ec-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="948ec-196">Proteger los recursos que más de un subproceso podría usar simultáneamente mediante secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="948ec-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="948ec-197">Utilizar la memoria local para el subproceso para el almacenamiento específico de subprocesos y sustituir las variables estáticas dentro de las funciones con variables locales para el subproceso.</span><span class="sxs-lookup"><span data-stu-id="948ec-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="948ec-198">Excel impone una restricción adicional: las funciones seguras para subprocesos no pueden registrarse como equivalentes de hojas de macros y, por lo tanto, no pueden llamar a funciones de información XLM u obtener los valores de las celdas no actualizadas.</span><span class="sxs-lookup"><span data-stu-id="948ec-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="948ec-199">Contención de memoria</span><span class="sxs-lookup"><span data-stu-id="948ec-199">Memory contention</span></span>
<span data-ttu-id="948ec-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="948ec-200"></span></span>

<span data-ttu-id="948ec-201">Los sistemas multiproceso deben resolver dos aspectos fundamentales:</span><span class="sxs-lookup"><span data-stu-id="948ec-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="948ec-202">Cómo proteger la memoria en la que más de un subproceso debe leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="948ec-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="948ec-203">Cómo crear y consultar memoria que esté asociada y reservada al subproceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="948ec-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="948ec-204">El sistema operativo Windows y el Kit de desarrollo de software de Windows ofrecen herramientas para las secciones críticas y la API de almacenamiento local de subprocesos (TLS) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="948ec-204">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively.</span></span> <span data-ttu-id="948ec-205">Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="948ec-205">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="948ec-206">El primer problema puede ocurrir, por ejemplo, cuando dos funciones de hoja de cálculo (o dos instancias de la misma función que se ejecutan simultáneamente) necesitan obtener acceso a la variable global o modificarla en un proyecto DLL.</span><span class="sxs-lookup"><span data-stu-id="948ec-206">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project.</span></span> <span data-ttu-id="948ec-207">Recuerde que esta variable global puede estar oculta en una instancia accesible globalmente de un objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="948ec-207">Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="948ec-208">El segundo problema puede ocurrir, por ejemplo, cuando una función de hoja de cálculo declara un objeto o una variable estática en el código del cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="948ec-208">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code.</span></span> <span data-ttu-id="948ec-209">El compilador de C o C ++ solo crea una sola copia que usan todas los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-209">The C/C++ compiler only creates a single copy that all threads use.</span></span> <span data-ttu-id="948ec-210">Esto significa que una instancia de la función podría cambiar el valor, mientras que otra en otro subproceso podría suponer que el valor es el que se estableció previamente.</span><span class="sxs-lookup"><span data-stu-id="948ec-210">This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="948ec-211">Aplicaciones de ejemplo de MTR</span><span class="sxs-lookup"><span data-stu-id="948ec-211">Example applications of MTR</span></span>
<span data-ttu-id="948ec-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="948ec-212"></span></span>

<span data-ttu-id="948ec-213">Cualquier XLL que exporte funciones de hoja de cálculo puede aprovechar las ventajas de la actualización multiproceso (MTR) en Excel, siempre y cuando esas funciones no necesiten realizar acciones no seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-213">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions.</span></span> <span data-ttu-id="948ec-214">Esto permite que Excel actualice los libros que dependen de ellos lo más rápido posible y, por lo tanto, es deseable cualquiera que sea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="948ec-214">This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="948ec-215">En concreto, MTR tiene un gran impacto en el tiempo actualización de los libros que llaman a funciones definidas por el usuario (UDF) que a su vez llaman a procesos externos para obtener el resultado deseado.</span><span class="sxs-lookup"><span data-stu-id="948ec-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="948ec-216">En concreto, considere una UDF que llama a un servidor remoto que puede procesar muchas solicitudes al mismo tiempo y un libro que contiene muchas llamadas a esa función.</span><span class="sxs-lookup"><span data-stu-id="948ec-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="948ec-217">Si la actualización de los libros es uniproceso, cada llamada a la UDF, y por ende al servidor remoto, debe completarse antes de que se pueda realizar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="948ec-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="948ec-218">Esto supone un desperdicio de la capacidad del servidor para procesar muchas llamadas a la vez.</span><span class="sxs-lookup"><span data-stu-id="948ec-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="948ec-219">Si la actualización del libro es multiproceso, Excel puede realizar varias llamadas al mismo tiempo o en rápida sucesión.</span><span class="sxs-lookup"><span data-stu-id="948ec-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="948ec-220">Si Excel se configura para usar el mismo número de subprocesos que el servidor (se le llama N) y la topología del árbol de dependencias del libro lo permite, el tiempo total de actualización podría reducirse a algo cercano a 1/N del tiempo de actualización uniproceso.</span><span class="sxs-lookup"><span data-stu-id="948ec-220">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time.</span></span> <span data-ttu-id="948ec-221">Esto puede ser verdadero incluso cuando el equipo cliente (en el que el libro se ejecuta) solo tiene un procesador, particularmente cuando el tiempo necesario para realizar la llamada al servidor es pequeño en relación con el tiempo que el servidor tarda en procesar la llamada.</span><span class="sxs-lookup"><span data-stu-id="948ec-221">This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="948ec-222">Hay una sobrecarga de sistema operativo para cada subproceso adicional.</span><span class="sxs-lookup"><span data-stu-id="948ec-222">There is operating system overhead for each additional thread.</span></span> <span data-ttu-id="948ec-223">Por lo tanto, puede necesitarse un poco de experimentación para que un libro determinado y un servidor y un equipo cliente determinados busquen el número óptimo de subprocesos que Excel puede usar.</span><span class="sxs-lookup"><span data-stu-id="948ec-223">Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="948ec-224">Por ejemplo, piense en un equipo con un solo procesador que ejecuta Excel y un libro que contiene 1000 celdas.</span><span class="sxs-lookup"><span data-stu-id="948ec-224">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells.</span></span> <span data-ttu-id="948ec-225">Este llama a una UDF, que a su vez llama a uno o más servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="948ec-225">It calls a UDF, which in turn calls one or more remote servers.</span></span> <span data-ttu-id="948ec-226">Suponga que las 1000 celdas no dependen unas de otras, de modo que Excel no tiene que esperar a que se complete una llamada para poder realizar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="948ec-226">Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next.</span></span> <span data-ttu-id="948ec-227">(Es posible relajar un poco esta restricción sin afectar a este ejemplo). Si los servidores pueden procesar 100 solicitudes al mismo tiempo, y Excel está configurado para usar 100 subprocesos, el tiempo de ejecución puede reducirse hasta 1/100 parte de aquel donde solo se usa un subproceso.</span><span class="sxs-lookup"><span data-stu-id="948ec-227">(Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used.</span></span> <span data-ttu-id="948ec-228">La sobrecarga que se asocia con Excel al asignar llamadas a cada subproceso y con el sistema operativo al administrar 100 subprocesos significa que, en la práctica, la reducción no será tan grande.</span><span class="sxs-lookup"><span data-stu-id="948ec-228">The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great.</span></span> <span data-ttu-id="948ec-229">También hay aquí un supuesto implícito de que el servidor se escala bien y, al solicitarle que procese 100 tareas al mismo tiempo, no se afectará significativamente a la finalización de tareas individuales.</span><span class="sxs-lookup"><span data-stu-id="948ec-229">There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="948ec-230">Una aplicación práctica en la que esta técnica puede tener una importante ventaja es la de los métodos de Monte Carlo, así como otras tareas numéricamente intensivas que se pueden dividir en subtareas más pequeñas que pueden asignarse a los servidores.</span><span class="sxs-lookup"><span data-stu-id="948ec-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="948ec-231">Consideraciones sobre Excel Services</span><span class="sxs-lookup"><span data-stu-id="948ec-231">Excel Services considerations</span></span>
<span data-ttu-id="948ec-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="948ec-232"></span></span>

<span data-ttu-id="948ec-233">Excel Services admite la carga, el cálculo y la representación de hojas de cálculo de Excel en un servidor.</span><span class="sxs-lookup"><span data-stu-id="948ec-233">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server.</span></span> <span data-ttu-id="948ec-234">Los usuarios pueden tener acceso a las hojas de cálculo e interactuar con ellas mediante herramientas estándar del explorador.</span><span class="sxs-lookup"><span data-stu-id="948ec-234">Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="948ec-235">Las UDF de Excel Services se crean con un código administrado de Microsoft .NET Framework y se publican a través de un ensamblado de .NET.</span><span class="sxs-lookup"><span data-stu-id="948ec-235">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly.</span></span> <span data-ttu-id="948ec-236">Los XLL no son compatibles con Excel Services.</span><span class="sxs-lookup"><span data-stu-id="948ec-236">XLLs are not supported by Excel Services.</span></span> <span data-ttu-id="948ec-237">Un recurso de UDF de servidor de código administrado puede llamar a un XLL para obtener acceso a su funcionalidad, de modo que el usuario puede tener la misma funcionalidad con un libro cargado en el servidor que con un libro cargado en el cliente.</span><span class="sxs-lookup"><span data-stu-id="948ec-237">A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="948ec-238">Por lo tanto, para disponer de las funciones de un XLL de esta forma, deben ajustarse en un ensamblado de .NET que convierta argumentos y valores devueltos de los tipos de datos nativos a los tipos de datos administrados de .NET Framework y que llame a las funciones XLL.</span><span class="sxs-lookup"><span data-stu-id="948ec-238">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions.</span></span> <span data-ttu-id="948ec-239">El contenedor de .NET exportará una UDF de servidor para cada función XLL a la que se tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="948ec-239">The .NET wrapper would export one server UDF for each XLL function being accessed.</span></span> <span data-ttu-id="948ec-240">Un requisito adicional es que las funciones XLL denominadas así deben ser seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-240">An additional requirement is that any XLL functions called in this way must be thread safe.</span></span> <span data-ttu-id="948ec-241">Dado que las funciones XLL no se registran de la misma forma que Excel del cliente, el servidor y el contenedor de .NET no tienen manera de exigir que sean seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="948ec-241">Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe.</span></span> <span data-ttu-id="948ec-242">Es responsabilidad del desarrollador de XLL garantizarlo.</span><span class="sxs-lookup"><span data-stu-id="948ec-242">It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="948ec-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="948ec-243">See also</span></span>

- [<span data-ttu-id="948ec-244">Actualización de Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-244">Excel recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="948ec-245">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="948ec-246">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-246">Accessing XLL code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="948ec-247">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="948ec-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="948ec-248">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="948ec-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

