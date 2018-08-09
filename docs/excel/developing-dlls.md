---
title: Desarrollar DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- archivos DLL [excel 2007], crear, crear archivos DLL [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815546"
---
# <a name="developing-dlls"></a><span data-ttu-id="4e476-104">Desarrollar DLL</span><span class="sxs-lookup"><span data-stu-id="4e476-104">Developing DLLs</span></span>

<span data-ttu-id="4e476-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4e476-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4e476-106">Una biblioteca es un cuerpo de código compilado que proporciona la funcionalidad y los datos a una aplicación ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4e476-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="4e476-107">Bibliotecas pueden ser vinculadas estáticamente o dinámicamente vinculadas y convencional tienen el lib de extensiones de nombre de archivo y .dll respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4e476-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="4e476-108">Bibliotecas estáticas (por ejemplo, la biblioteca de tiempo de ejecución de C) están vinculadas a la aplicación en la compilación y por lo que se convierten en parte del archivo ejecutable resultante.</span><span class="sxs-lookup"><span data-stu-id="4e476-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="4e476-109">La aplicación carga un archivo DLL cuando es necesario, normalmente, cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e476-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="4e476-110">Un archivo DLL puede cargar y vincular dinámicamente a otro archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="4e476-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="4e476-111">Ventajas del uso de archivos DLL</span><span class="sxs-lookup"><span data-stu-id="4e476-111">Benefits of using DLLs</span></span>

<span data-ttu-id="4e476-112">Los principales beneficios de DLL son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e476-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="4e476-113">Todas las aplicaciones pueden compartir una única copia en el disco.</span><span class="sxs-lookup"><span data-stu-id="4e476-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="4e476-114">Archivos ejecutables de aplicaciones se conservan más pequeños.</span><span class="sxs-lookup"><span data-stu-id="4e476-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="4e476-115">Permiten que los proyectos de desarrollo de gran tamaño dividir.</span><span class="sxs-lookup"><span data-stu-id="4e476-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="4e476-116">Los desarrolladores de aplicaciones y DLL sólo necesitan acepta una interfaz entre sus elementos respectivos.</span><span class="sxs-lookup"><span data-stu-id="4e476-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="4e476-117">Esta interfaz es exportada por el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="4e476-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="4e476-118">Los programadores DLL pueden actualizar los archivos DLL: quizás para hacerlas más eficaz o para corregir un error, sin tener que actualizar todas las aplicaciones que usan, siempre que no cambie la interfaz exportada del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="4e476-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="4e476-119">Puede usar archivos DLL para agregar comandos y funciones de hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4e476-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="4e476-120">Recursos para la creación de archivos DLL</span><span class="sxs-lookup"><span data-stu-id="4e476-120">Resources for creating DLLs</span></span>

<span data-ttu-id="4e476-121">Para crear un archivo DLL, se necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e476-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="4e476-122">Un editor de código fuente.</span><span class="sxs-lookup"><span data-stu-id="4e476-122">A source code editor.</span></span>
    
- <span data-ttu-id="4e476-123">Un compilador para convertir código fuente en el código de objeto que es compatible con su hardware.</span><span class="sxs-lookup"><span data-stu-id="4e476-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="4e476-124">Un vinculador para agregar código de bibliotecas estáticas, dónde se usa y para crear el archivo ejecutable de DLL.</span><span class="sxs-lookup"><span data-stu-id="4e476-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="4e476-125">Entornos de moderno de desarrollo integrado (IDE), como Microsoft Visual Studio, proporcionan todas estas cosas.</span><span class="sxs-lookup"><span data-stu-id="4e476-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="4e476-126">También proporcionan mucho más información: inteligentes editores, herramientas para depurar el código, herramientas para administrar varios proyectos, los nuevos asistentes para proyectos y muchas otras herramientas importantes.</span><span class="sxs-lookup"><span data-stu-id="4e476-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="4e476-127">Puede crear archivos DLL en varios idiomas, por ejemplo, C o C++, Pascal y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e476-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="4e476-128">Dado que el código de origen de la API que se proporcionan con Excel es C y C++, sólo estos dos lenguajes se consideran en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="4e476-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="4e476-129">Exportación de funciones y comandos</span><span class="sxs-lookup"><span data-stu-id="4e476-129">Exporting functions and commands</span></span>

<span data-ttu-id="4e476-130">Cuando se compila un proyecto de DLL, el compilador y el vinculador deben saber cuáles son las funciones que se exportará para que pueden que estén disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e476-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="4e476-131">En esta sección se describe las maneras en que esto se puede hacer.</span><span class="sxs-lookup"><span data-stu-id="4e476-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="4e476-132">Cuando los compiladores compilación el código fuente, en general, cambian los nombres de las funciones de su aspecto en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="4e476-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="4e476-133">Normalmente hacen esto agregando al principio y al final del nombre, en un proceso conocido como decoración de nombres.</span><span class="sxs-lookup"><span data-stu-id="4e476-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="4e476-134">Debe asegurarse de que la función se exporta con un nombre que puedan reconocer a la aplicación al cargar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="4e476-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="4e476-135">Esto puede significar que indica el vinculador para asociar el nombre decorado con un nombre de exportación más sencillo.</span><span class="sxs-lookup"><span data-stu-id="4e476-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="4e476-136">El nombre de exportación puede ser el nombre tal como aparecía originalmente en el código fuente, o algo más.</span><span class="sxs-lookup"><span data-stu-id="4e476-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="4e476-137">La forma en que el nombre está decorado depende del idioma y cómo se indica el compilador para que la función esté disponible, es decir, la convención de llamada.</span><span class="sxs-lookup"><span data-stu-id="4e476-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="4e476-138">La convención de llamada entre procesos estándar de Windows utilizado por archivos DLL se conoce como la convención de WinAPI.</span><span class="sxs-lookup"><span data-stu-id="4e476-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="4e476-139">Se define en archivos de encabezado de Windows como **WINAPI**, lo que a su vez se define mediante el declarador de Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="4e476-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="4e476-140">Una función de exportación de DLL para su uso con Excel (si es una función de hoja de cálculo, la hoja de macros equivalente de la función o el comando definido por el usuario) debe utilizar siempre el **WINAPI** / convención de llamada **__stdcall** .</span><span class="sxs-lookup"><span data-stu-id="4e476-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="4e476-141">Es necesario incluir el especificador **WINAPI** explícitamente en la definición de la función como el valor predeterminado en Win32 compiladores consiste en usar la **__cdecl** convención de llamada, que también se define como **WINAPIV**, si no se especifica ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e476-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="4e476-142">Puede saber el vinculador que es una función que se va a exportar y el nombre es que es conocida por externamente en una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="4e476-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="4e476-143">Colocar la función en un archivo de definición después de la palabra clave de **exportaciones** y establecer la configuración del proyecto DLL para hacer referencia a este archivo cuando la vinculación.</span><span class="sxs-lookup"><span data-stu-id="4e476-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="4e476-144">Use el declarador **__declspec (dllexport)** en la definición de la función.</span><span class="sxs-lookup"><span data-stu-id="4e476-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="4e476-145">Use una directiva de preprocesador **#pragma** para enviar un mensaje al vinculador.</span><span class="sxs-lookup"><span data-stu-id="4e476-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="4e476-146">Aunque el proyecto puede usar los tres métodos y el compilador y el vinculador admiten, no debe intentar exportar una función de más de una de estas formas.</span><span class="sxs-lookup"><span data-stu-id="4e476-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="4e476-147">Por ejemplo, supongamos que un archivo DLL contiene módulos de código de origen de dos, uno C y uno C++, que contienen dos funciones que se va a exportar, **Mi\_C\_exportar** y **Mis\_Cpp\_exportar** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4e476-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="4e476-148">Por motivos de simplicidad, suponga que cada función toma un único argumento numérico de doble precisión y devuelve el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4e476-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="4e476-149">Las alternativas para la exportación de cada función mediante el uso de cada uno de estos métodos se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="4e476-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="4e476-150">Uso de un archivo de definición</span><span class="sxs-lookup"><span data-stu-id="4e476-150">Using a DEF file</span></span>

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

<span data-ttu-id="4e476-151">El archivo de definición, a continuación, tendría que contienen estas líneas.</span><span class="sxs-lookup"><span data-stu-id="4e476-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="4e476-152">La sintaxis general de una línea que sigue a una instrucción **exportaciones** es como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4e476-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="4e476-153">Tenga en cuenta que la función C se ha decorado, pero el archivo DEF fuerza explícitamente el vinculador para exponer la función con el nombre de código de origen original (en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="4e476-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="4e476-154">El vinculador implícitamente exporta la función C++ usando el nombre original del código, por lo que no es necesario incluir el nombre decorado en el archivo de definición.</span><span class="sxs-lookup"><span data-stu-id="4e476-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="4e476-155">Para llamadas de función de la API de Windows de 32 bits, la convención para la decoración de funciones compiladas C es como sigue: **nombre_de_función** se convierte en _ **nombre_de_función @** _n_ donde _n_ es el número de bytes, expresado como un valor decimal que ocupan todos los argumentos, con los bytes para cada uno de ellos se redondea hacia arriba hasta el múltiplo más cercano de cuatro.</span><span class="sxs-lookup"><span data-stu-id="4e476-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e476-156">Todos los punteros son ancho en Win32 de cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="4e476-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="4e476-157">El tipo de valor devuelto tiene ningún efecto en la decoración de nombres.</span><span class="sxs-lookup"><span data-stu-id="4e476-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="4e476-158">Es posible forzar el compilador de C++ para exponer los nombres no representativos para funciones de C++ al incluir la función y los prototipos de función, dentro de un extern "C" {...}</span><span class="sxs-lookup"><span data-stu-id="4e476-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="4e476-159">bloquear, tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e476-159">block, as shown in this example.</span></span> <span data-ttu-id="4e476-160">(Las llaves **{}** se omiten aquí debido a que la declaración sólo hace referencia al bloque de código de función que inmediatamente a continuación).</span><span class="sxs-lookup"><span data-stu-id="4e476-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="4e476-161">Cuando se va a colocar los prototipos de función de C en archivos de encabezado que podrían estar incluidos en archivos de origen de C o C++, debe incluir la siguiente directiva de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4e476-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
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

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="4e476-162">Utilizando el declarador __declspec (dllexport)</span><span class="sxs-lookup"><span data-stu-id="4e476-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="4e476-163">La palabra clave **__declspec (dllexport)** se puede usar en la declaración de la función de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="4e476-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="4e476-164">La palabra clave **__declspec (dllexport)** debe agregarse en el extremo izquierdo de la declaración.</span><span class="sxs-lookup"><span data-stu-id="4e476-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="4e476-165">Las ventajas de este enfoque son que la función no es necesario que se mostrarán en un archivo de definición, y que el estado de exportación es el adecuado con la definición.</span><span class="sxs-lookup"><span data-stu-id="4e476-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="4e476-166">Si desea evitar una función de C++ va a estar disponible con el adorno de nombre de C++, debe declarar la función de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="4e476-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="4e476-167">El vinculador hará que la función está disponible como my_undecorated_Cpp_export, es decir, el nombre tal como aparece en el código fuente con ningún adorno.</span><span class="sxs-lookup"><span data-stu-id="4e476-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="4e476-168">Uso de una directiva de preprocesador vinculador #pragma</span><span class="sxs-lookup"><span data-stu-id="4e476-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="4e476-169">Versiones más recientes de Microsoft Visual Studio admiten dos macros predefinidas que, cuando se usa junto con una directiva **#pragma** , permiten indicar el vinculador para exportar la función directamente desde el código de función.</span><span class="sxs-lookup"><span data-stu-id="4e476-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="4e476-170">Las macros están __(función)__ y __FUNCDNAME__ (tenga en cuenta el subrayado doble al final de cada) que se expanden a los nombres de función decorado y no decorado respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4e476-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="4e476-171">Por ejemplo, cuando se usa Microsoft Visual Studio, estas líneas pueden incorporarse en un archivo de encabezado comunes como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4e476-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="4e476-172">Si este encabezado está incluido en los archivos de origen, las funciones de dos ejemplo, a continuación, se pueden exportar como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4e476-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="4e476-173">Código de C:</span><span class="sxs-lookup"><span data-stu-id="4e476-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="4e476-174">Código de C++:</span><span class="sxs-lookup"><span data-stu-id="4e476-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="4e476-175">Tenga en cuenta que la directiva debe ubicarse dentro del cuerpo de la función y sólo se expande cuando ninguna de las opciones del compilador se **establece/EP** **o/p** .</span><span class="sxs-lookup"><span data-stu-id="4e476-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="4e476-176">Esta técnica elimina la necesidad de un archivo de definición o declaración **__declspec (dllexport)** y mantiene la especificación de su estado de exportación con el código de función.</span><span class="sxs-lookup"><span data-stu-id="4e476-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e476-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e476-177">See also</span></span>

- [<span data-ttu-id="4e476-178">Obtener acceso a DLL en Excel</span><span class="sxs-lookup"><span data-stu-id="4e476-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="4e476-179">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="4e476-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="4e476-180">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="4e476-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="4e476-181">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="4e476-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

