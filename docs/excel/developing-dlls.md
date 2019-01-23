---
title: Desarrollar bibliotecas DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- bibliotecas dll [excel 2007], crear, crear bibliotecas DLL [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704752"
---
# <a name="developing-dlls"></a><span data-ttu-id="0005d-104">Desarrollar bibliotecas DLL</span><span class="sxs-lookup"><span data-stu-id="0005d-104">Developing DLLs</span></span>

<span data-ttu-id="0005d-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0005d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0005d-106">Una biblioteca es un cuerpo de código compilado que proporciona alguna funcionalidad y datos a una aplicación ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0005d-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="0005d-107">Las bibliotecas pueden estar vinculadas estáticamente o dinámicamente y tienen convencionalmente extensiones de nombre de archivo .lib y .dll respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0005d-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="0005d-108">Las bibliotecas estáticas (por ejemplo, la biblioteca en tiempo de ejecución de C) están vinculadas a la aplicación en la compilación y así se convierten en parte del ejecutable resultante.</span><span class="sxs-lookup"><span data-stu-id="0005d-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="0005d-109">La aplicación carga una DLL cuando es necesario, normalmente, cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0005d-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="0005d-110">Una DLL puede cargarse y vincularse dinámicamente con otra DLL.</span><span class="sxs-lookup"><span data-stu-id="0005d-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="0005d-111">Ventajas de usar las DLL </span><span class="sxs-lookup"><span data-stu-id="0005d-111">Benefits of using MDS</span></span>

<span data-ttu-id="0005d-112">Las principales ventajas de las DLL son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0005d-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="0005d-113">Todas las aplicaciones pueden compartir una única copia en el disco.</span><span class="sxs-lookup"><span data-stu-id="0005d-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="0005d-114">Los archivos ejecutables de las aplicaciones se mantienen más pequeños.</span><span class="sxs-lookup"><span data-stu-id="0005d-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="0005d-115">Permiten dividir los proyectos de desarrollo de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="0005d-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="0005d-116">Los desarrolladores de aplicaciones y DLL solo necesitan acordar una interfaz entre los elementos respectivos.</span><span class="sxs-lookup"><span data-stu-id="0005d-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="0005d-117">La DLL exporta esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0005d-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="0005d-118">Los desarrolladores DLL pueden actualizar las DLL, por ejemplo para que sean más eficientes o para corregir un error, sin tener que actualizar todas las aplicaciones que las usan, siempre que no cambie la interfaz de la DLL exportada.</span><span class="sxs-lookup"><span data-stu-id="0005d-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="0005d-119">Puede usar bibliotecas DLL para agregar comandos y funciones de hoja de cálculo en Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0005d-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="0005d-120">Recursos para crear las DLL</span><span class="sxs-lookup"><span data-stu-id="0005d-120">Resources for creating DLLs</span></span>

<span data-ttu-id="0005d-121">Para crear una DLL, necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0005d-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="0005d-122">Un editor de código fuente.</span><span class="sxs-lookup"><span data-stu-id="0005d-122">A source code editor.</span></span>
    
- <span data-ttu-id="0005d-123">Un compilador para convertir el código fuente en el código de objeto que es compatible con el hardware.</span><span class="sxs-lookup"><span data-stu-id="0005d-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="0005d-124">Un vinculador para agregar código de bibliotecas estáticas, donde se usan, y para crear el archivo DLL ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0005d-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="0005d-125">Los entornos de desarrollo integrado (IDE) modernos, como Microsoft Visual Studio, proporcionan estos elementos.</span><span class="sxs-lookup"><span data-stu-id="0005d-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="0005d-126">También proporcionan mucho más: editores inteligentes, herramientas para depurar el código, herramientas para administrar varios proyectos, nuevos asistentes de proyectos y muchas otras herramientas importantes.</span><span class="sxs-lookup"><span data-stu-id="0005d-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="0005d-127">Puede crear bibliotecas DLL en varios lenguajes, por ejemplo, C o C++, Pascal y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0005d-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="0005d-128">Como el código fuente de la API proporcionado con Excel es en C y C++, se consideran solo estos dos lenguajes en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="0005d-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="0005d-129">Exportar comandos y funciones</span><span class="sxs-lookup"><span data-stu-id="0005d-129">Exporting functions and commands</span></span>

<span data-ttu-id="0005d-130">Al compilar un proyecto DLL, el compilador y vinculador necesitan saber cuáles son las funciones para exportar para que puedan estar disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0005d-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="0005d-131">Esta sección describe las maneras para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="0005d-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="0005d-132">Cuando los compiladores compilan el código fuente, por lo general, cambian los nombres de las funciones en el mismo.</span><span class="sxs-lookup"><span data-stu-id="0005d-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="0005d-133">Normalmente hacen esto agregando elementos al principio o al final del nombre, en un proceso denominado decoración de nombres.</span><span class="sxs-lookup"><span data-stu-id="0005d-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="0005d-134">Deberá asegurarse de que la función se exporta con un nombre que la aplicación que carga la DLL pueda reconocer.</span><span class="sxs-lookup"><span data-stu-id="0005d-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="0005d-135">Esto puede significar indicarle al vinculador que asocie al nombre representativo un nombre de exportación más sencillo.</span><span class="sxs-lookup"><span data-stu-id="0005d-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="0005d-136">El nombre de exportación puede ser el mismo nombre que aparecía originalmente en el código fuente u otro.</span><span class="sxs-lookup"><span data-stu-id="0005d-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="0005d-137">La manera de crear un nombre representativo depende del lenguaje y de cómo se indica al compilador que ponga la función a disposición, es decir, la convención de llamada.</span><span class="sxs-lookup"><span data-stu-id="0005d-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="0005d-138">La convención de llamada entre procesos estándar para Windows que usan las DLL se conoce como la convención WinAPI.</span><span class="sxs-lookup"><span data-stu-id="0005d-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="0005d-139">Se define en archivos de encabezado de Windows como **WINAPI**, que a su vez se define con el declarador Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="0005d-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="0005d-140">Para usar una función de exportación de DLL ( ya sea una función de hoja de cálculo, una función de hoja macro equivalente o un comando definido por el usuario) en Excel, debe usar siempre la convención de llamada **WINAPI** / **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="0005d-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="0005d-141">Es necesario incluir el especificador **WINAPI** explícitamente en la definición de la función porque en los compiladores Win32 se usa de forma predeterminada la convención de llamada **__cdecl**, que también se define como \*\* WINAPIV\*\*, si no se especifica ninguna.</span><span class="sxs-lookup"><span data-stu-id="0005d-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="0005d-142">Puede indicar al vinculador que se va a exportar una función y que el nombre se debe conocer externamente mediante uno de los siguientes métodos. Es posible:</span><span class="sxs-lookup"><span data-stu-id="0005d-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="0005d-143">Colocar la función de un archivo DEF después de la palabra clave **EXPORTS** y establecer la configuración del proyecto DLL para que haga referencia a este archivo al realizar el vínculo.</span><span class="sxs-lookup"><span data-stu-id="0005d-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="0005d-144">Usar el declarador **__declspec(dllexport)** en la definición de la función.</span><span class="sxs-lookup"><span data-stu-id="0005d-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="0005d-145">Usar una directiva de preprocesador **#pragma** para enviar un mensaje al vinculador.</span><span class="sxs-lookup"><span data-stu-id="0005d-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="0005d-146">Aunque el proyecto puede usar los tres métodos y su compilador y vinculador son compatibles con los tres, no debería intentar exportar una función con más de uno de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0005d-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="0005d-147">Por ejemplo, supongamos que una DLL contiene dos módulos de código fuente, uno en C y otro en C++, que contienen dos funciones para exportar, **my\_C\_export** y **my\_Cpp\_export** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0005d-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="0005d-148">Para simplificar, supongamos que cada función toma un único argumento numérico de doble precisión y devuelve el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0005d-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="0005d-149">En las siguientes secciones se describen las alternativas para exportar cada función con cada uno de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0005d-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="0005d-150">Usar un archivo DEF</span><span class="sxs-lookup"><span data-stu-id="0005d-150">Using a DEF file</span></span>

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

<span data-ttu-id="0005d-151">El archivo DEF necesitaría contener estas líneas.</span><span class="sxs-lookup"><span data-stu-id="0005d-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="0005d-152">La sintaxis general de la línea que sigue a una instrucción **EXPORTS** es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="0005d-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="0005d-153">Tenga en cuenta que la función C tiene un nombre representativo, pero el archivo DEF obliga explícitamente al vinculador que exponga la función con el nombre del código fuente original (en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="0005d-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="0005d-154">El vinculador implícitamente exporta la función C++ usando el nombre de código original, por lo que no es necesario incluir el nombre representativo en el archivo DEF.</span><span class="sxs-lookup"><span data-stu-id="0005d-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="0005d-155">Para llamadas de función de la API de Windows de 32 bits, la convención para la asignación de un nombre representativo a funciones compiladas en C es la siguiente: **nombre_de_función** se convierte en _ **nombre_de_función @** _n_ donde _n_ es el número de bytes, expresado como un número decimal usado por todos los argumentos, para cada cual los bytes se redondean al múltiplo más cercano de cuatro. </span><span class="sxs-lookup"><span data-stu-id="0005d-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0005d-156">Todos los punteros son de cuatro bytes de ancho en Win32.</span><span class="sxs-lookup"><span data-stu-id="0005d-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="0005d-157">El tipo de valor devuelto no tiene impacto en la decoración de nombres.</span><span class="sxs-lookup"><span data-stu-id="0005d-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="0005d-158">Es posible forzar al compilador de C++ que no exponga los nombres representativos de las funciones de C++ escribiendo la función y cualquier prototipo de función dentro de un bloque "C" {...} </span><span class="sxs-lookup"><span data-stu-id="0005d-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="0005d-159">externo, como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0005d-159">block, as shown in this example.</span></span> <span data-ttu-id="0005d-160">(Las llaves **{}** se omiten aquí porque la declaración sólo hace referencia al bloque de código de la función que sigue inmediatamente).</span><span class="sxs-lookup"><span data-stu-id="0005d-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="0005d-161">Cuando se colocan prototipos de función de C en archivos de encabezado que pueden incluirse en archivos de origen de C o C++, debe incluirse la directiva de preprocesador siguiente.</span><span class="sxs-lookup"><span data-stu-id="0005d-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="0005d-162">Usar el declarador __declspec(dllexport)</span><span class="sxs-lookup"><span data-stu-id="0005d-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="0005d-163">La palabra clave **__declspec(dllexport)** puede usarse en la declaración de la función como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0005d-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="0005d-164">La palabra clave **__declspec(dllexport)** debe agregarse en el extremo izquierdo de la declaración.</span><span class="sxs-lookup"><span data-stu-id="0005d-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="0005d-165">Las ventajas de este método son que no es necesario que la función esté incluida en un archivo DEF y que el estado de exportación se encuentra con la definición.</span><span class="sxs-lookup"><span data-stu-id="0005d-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="0005d-166">Si quiere evitar que una función C++ esté disponible con un nombre representativo de C++, debe declarar la función como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0005d-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="0005d-167">El vinculador pondrá a disposición la función como my_undecorated_Cpp_export, es decir, el nombre que aparece en el código fuente sin ninguna decoración.</span><span class="sxs-lookup"><span data-stu-id="0005d-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="0005d-168">Usar la directiva del vinculador del preprocesador #pragma</span><span class="sxs-lookup"><span data-stu-id="0005d-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="0005d-169">Versiones más recientes de Microsoft Visual Studio admiten dos macros predefinidas que, cuando se usan junto con una directiva **#pragma**, permiten indicar al vinculador que exporte la función directamente desde el código de función.</span><span class="sxs-lookup"><span data-stu-id="0005d-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="0005d-170">Las macros son __FUNCTION__ y __FUNCDNAME__ (tenga en cuenta el subrayado doble de los extremos) que se expanden a los nombres de función no representativos y representativos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0005d-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="0005d-171">Por ejemplo, si usa Microsoft Visual Studio, estas líneas pueden incorporarse a un archivo de encabezado común como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0005d-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="0005d-172">Si se incluye este encabezado en los archivos de origen, las dos funciones de ejemplo se pueden exportar como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0005d-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="0005d-173">Código C:</span><span class="sxs-lookup"><span data-stu-id="0005d-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="0005d-174">Código C++:</span><span class="sxs-lookup"><span data-stu-id="0005d-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="0005d-175">Tenga en cuenta que la directiva debe incluirse en el cuerpo de la función y sólo se expande si ninguna de las opciones **/EP** o **/P** está configurada.</span><span class="sxs-lookup"><span data-stu-id="0005d-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="0005d-176">Esta técnica elimina la necesidad de un archivo DEF o una declaración **__declspec(dllexport)** y se mantiene la especificación de su estado de exportación con el código de la función.</span><span class="sxs-lookup"><span data-stu-id="0005d-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0005d-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="0005d-177">See also</span></span>

- [<span data-ttu-id="0005d-178">Obtener acceso a las DLL en Excel</span><span class="sxs-lookup"><span data-stu-id="0005d-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="0005d-179">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="0005d-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="0005d-180">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="0005d-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="0005d-181">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="0005d-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

