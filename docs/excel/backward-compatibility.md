---
title: Compatibilidad con versiones anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidad de versiones [Excel 2007], compatibilidad de XLL [Excel 2007], compatibilidad con versiones anteriores [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301683"
---
# <a name="backward-compatibility"></a><span data-ttu-id="096df-104">Compatibilidad con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="096df-104">Backward compatibility</span></span>

<span data-ttu-id="096df-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="096df-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="096df-106">En este tema se tratan los problemas de compatibilidad de XLL en diferentes versiones de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="096df-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="096df-107">Definiciones de constantes útiles</span><span class="sxs-lookup"><span data-stu-id="096df-107">Useful constant definitions</span></span>

<span data-ttu-id="096df-108">Considere la posibilidad de incluir definiciones similares a estas en el código del proyecto XLL y reemplazar todas las instancias de números literales que se usan en este contexto.</span><span class="sxs-lookup"><span data-stu-id="096df-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="096df-109">Esto clarificará el código que es específico de la versión y reduce la probabilidad de errores relacionados con la versión en forma de números inocuos.</span><span class="sxs-lookup"><span data-stu-id="096df-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="096df-110">Obtener la versión en ejecución</span><span class="sxs-lookup"><span data-stu-id="096df-110">Getting the running version</span></span>

<span data-ttu-id="096df-111">Debe detectar qué versión se está ejecutando usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, donde `arg` es un **XLOPER** numérico establecido en 2 y version es una cadena **XLOPER** que, a continuación, se puede convertir en un entero.</span><span class="sxs-lookup"><span data-stu-id="096df-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="096df-112">Para Microsoft Excel 2013, es 15,0.</span><span class="sxs-lookup"><span data-stu-id="096df-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="096df-113">Debe hacer esto en la función [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="096df-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="096df-114">A continuación, puede establecer una variable global que informe de todos los módulos del proyecto en el que se está ejecutando la versión de Excel.</span><span class="sxs-lookup"><span data-stu-id="096df-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="096df-115">A continuación, el código puede decidir si desea llamar a la API de C mediante **Excel12** y **XLOPER12**s, o usar **Excel4** con **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="096df-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="096df-116">Puede llamar a **XLCallVer** para descubrir la versión de la API de C, pero esto no indica qué versiones de las versiones anteriores a Excel 2007 está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="096df-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="096df-117">Creación de complementos que exportan interfaces duales</span><span class="sxs-lookup"><span data-stu-id="096df-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="096df-118">Considere una función XLL que toma una cadena y devuelve un valor que puede ser cualquiera de los tipos de datos de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="096df-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="096df-119">Puede exportar una función registrada como tipo "PD" y con prototipos como se indica a continuación, donde la cadena se pasa como una cadena de bytes de longitud contada.</span><span class="sxs-lookup"><span data-stu-id="096df-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="096df-120">Aunque esto funciona perfectamente, hay varias razones por las que esta no es la interfaz ideal para el código a partir de Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="096df-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="096df-121">Está sujeta a las limitaciones de las cadenas de bytes de la API de C y no puede tener acceso a las cadenas Unicode largas admitidas a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="096df-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="096df-122">Aunque, a partir de Excel 2007, Excel puede pasar y aceptar **XLOPER**, los convierte internamente a **XLOPER12**s, por lo que hay una sobrecarga de conversión implícita a partir de Excel 2007 que no está allí cuando el código se ejecuta en versiones anteriores de Excel.</span><span class="sxs-lookup"><span data-stu-id="096df-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="096df-123">Puede que esta función sea segura para la realización de subprocesos, pero si se cambia la cadena `PD$`del tipo a, se produce un error en el registro al iniciarse antes de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="096df-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="096df-124">Por estos motivos, idealmente, a partir de Excel 2007, debe exportar una función a los usuarios que se registraron `QD%$`como, suponiendo que el código es seguro para subprocesos y prototipos de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="096df-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="096df-125">Otro motivo por el que es posible que desee registrar una función diferente que comienza en Excel 2007 es que permite que las funciones XLL puedan tardar hasta 255 argumentos, en lugar del límite 30 de versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="096df-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="096df-126">Afortunadamente, puede tener las ventajas de ambas mediante la exportación de ambas versiones desde el proyecto.</span><span class="sxs-lookup"><span data-stu-id="096df-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="096df-127">A continuación, puede detectar la versión de Excel en ejecución y registrar condicionalmente la función más adecuada.</span><span class="sxs-lookup"><span data-stu-id="096df-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="096df-128">Para obtener más información y una implementación de ejemplo, consulte [developIng Add-Ins (XLL) en Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="096df-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="096df-129">Este enfoque conduce a la posibilidad de que una hoja de cálculo que se ejecute en Excel 2003 pueda mostrar resultados distintos de la misma hoja que se está iniciando en Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="096df-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="096df-130">Por ejemplo, Excel 2003 asignaría una cadena Unicode en una celda de la hoja de cálculo de Excel 2003 a una cadena de bytes ASCII y la truncaría antes de pasarla a una función XLL.</span><span class="sxs-lookup"><span data-stu-id="096df-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="096df-131">A partir de Excel 2007, Excel pasará una cadena Unicode no convertida a una función XLL registrada de la forma correcta.</span><span class="sxs-lookup"><span data-stu-id="096df-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="096df-132">Esto puede provocar un resultado diferente.</span><span class="sxs-lookup"><span data-stu-id="096df-132">This could lead to a different result.</span></span> <span data-ttu-id="096df-133">Debe tener en cuenta esta posibilidad y las consecuencias para los usuarios, no solo en la actualización.</span><span class="sxs-lookup"><span data-stu-id="096df-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="096df-134">Por ejemplo, algunas funciones numéricas integradas se mejoraron entre Excel 2000 y Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="096df-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="096df-135">Nuevas funciones de hoja de cálculo y herramientas de análisis</span><span class="sxs-lookup"><span data-stu-id="096df-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="096df-136">Las funciones de herramientas de análisis (ATP) forman parte de Excel a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="096df-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="096df-137">Anteriormente, un XLL solo podía llamar a una función ATP mediante [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="096df-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="096df-138">A partir de Excel 2007, se debe llamar a las funciones de ATP con las enumeraciones de función definidas en xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="096df-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="096df-139">El ejemplo en el que se llama a funciones definidas por el usuario desde dll muestra los dos métodos diferentes.</span><span class="sxs-lookup"><span data-stu-id="096df-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="096df-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="096df-140">See also</span></span>

- [<span data-ttu-id="096df-141">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="096df-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="096df-142">Programar con la API de C en Excel</span><span class="sxs-lookup"><span data-stu-id="096df-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="096df-143">Novedades de la API de C para Excel</span><span class="sxs-lookup"><span data-stu-id="096df-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

