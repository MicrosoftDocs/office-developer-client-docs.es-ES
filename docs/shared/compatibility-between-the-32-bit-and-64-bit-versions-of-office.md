---
title: Compatibilidad entre versiones de 32 y 64 bits de Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra cómo la versión de 32 bits de Office es compatible con la versión de 64 bits de Office.
ms.openlocfilehash: eeff11f11d4f2595b7111c0233703d09b1c46651
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390943"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="d8337-103">Compatibilidad entre versiones de 32 y 64 bits de Office</span><span class="sxs-lookup"><span data-stu-id="d8337-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="d8337-104">Descubra cómo la versión de 32 bits de Office es compatible con la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="d8337-105">Las aplicaciones de Office están disponibles en versiones de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="d8337-106">Las versiones de 64 bits de Office permiten mover los datos más de una mayor capacidad de, por ejemplo, cuando se trabaja con un gran número de Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="d8337-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="d8337-107">Al escribir código de 32 bits, puede usar la versión de 64 bits de Office sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d8337-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="d8337-108">Sin embargo, cuando se escribe código de 64 bits, debe asegurarse de que el código contiene palabras clave específicas y las constantes de compilación condicional para asegurarse de que el código es compatible con la versión anterior de Office y que se está ejecutando el código correcto si se mezclar código de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="d8337-109">Visual Basic para aplicaciones 7.0 (VBA 7) está publicado en las versiones de 64 bits para Office y funciona con aplicaciones de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="d8337-110">Los cambios que se describen en este artículo se aplican sólo a las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="d8337-111">Con las versiones de 32 bits de habilitar Microsoft Office utilizar soluciones creadas en versiones anteriores de Office sin modificaciones aún más.</span><span class="sxs-lookup"><span data-stu-id="d8337-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d8337-112">De forma predeterminada, al instalar una versión de 64 bits de Office, se instala también la versión de 32 bits se instala junto con el sistema de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="d8337-113">Debe seleccionar explícitamente la opción de instalación de la versión de Microsoft Office de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="d8337-114">En VBA 7, debe actualizar las instrucciones de API de Windows (instrucciones**Declare** ) existentes para que funcione con la versión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="d8337-115">Además, debe actualizar punteros de dirección y mostrar los identificadores de ventana en tipos definidos por el usuario que se usan por estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="d8337-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="d8337-116">Esto se describe con más detalle en este artículo, así como problemas de compatibilidad entre las versiones de 32 bits y 64 bits y soluciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="d8337-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="d8337-117">Comparación de los sistemas de 32 bits y 64 bits</span><span class="sxs-lookup"><span data-stu-id="d8337-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="d8337-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-118"></span></span>

<span data-ttu-id="d8337-119">Las aplicaciones creadas con las versiones de 64 bits de Office pueden hacer referencia a los espacios de direcciones mayores que las versiones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="d8337-120">Esto significa que se puede usar más memoria física para los datos que antes, puede reducir la sobrecarga de empleado en mover datos dentro y fuera de la memoria física</span><span class="sxs-lookup"><span data-stu-id="d8337-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="d8337-121">Además de hacer referencia a ubicaciones específicas (conocidas como punteros) en la memoria física, también puede utilizar direcciones para hacer referencia a identificadores de ventana para mostrar (conocidos como identificadores).</span><span class="sxs-lookup"><span data-stu-id="d8337-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="d8337-122">El tamaño (en bytes) del puntero o identificador depende de si está utilizando un sistema de 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="d8337-123">Si desea ejecutar las soluciones existentes con las versiones de 64 bits de Office, tenga en cuenta de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="d8337-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="d8337-124">Procesos de 64 bits nativos de Office no pueden cargar los archivos binarios de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="d8337-125">Esto se espera que un problema común cuando haya existentes controles Microsoft ActiveX y complementos existentes.</span><span class="sxs-lookup"><span data-stu-id="d8337-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="d8337-126">VBA anteriormente no tiene un tipo de datos de puntero, por lo que había que usar variables de 32 bits para almacenar punteros e identificadores.</span><span class="sxs-lookup"><span data-stu-id="d8337-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="d8337-127">Estas variables ahora truncan valores de 64 bits devueltos por llamadas a la API cuando se usa instrucciones **Declare** .</span><span class="sxs-lookup"><span data-stu-id="d8337-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="d8337-128">Base de código VBA 7</span><span class="sxs-lookup"><span data-stu-id="d8337-128">VBA 7 code base</span></span>
<span data-ttu-id="d8337-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-129"></span></span>

<span data-ttu-id="d8337-130">VBA 7 reemplaza el código VBA que se base en Office 2007 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d8337-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="d8337-131">7 de VBA está disponible en las versiones de 32 bits y 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="d8337-132">Proporciona dos constantes de compilación condicional:</span><span class="sxs-lookup"><span data-stu-id="d8337-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="d8337-133">**VBA7** - ayuda a garantizar la compatibilidad con versiones anteriores del código mediante la comprobación de si la aplicación usa VBA 7 o la versión anterior de VBA.</span><span class="sxs-lookup"><span data-stu-id="d8337-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="d8337-134">**Win64** Comprueba si se ejecuta el código como 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="d8337-135">Con algunas excepciones, las macros de un documento que funcionan en la versión de 32 bits de la aplicación también funcionan con la versión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="d8337-136">Control ActiveX y compatibilidad de complementos COM</span><span class="sxs-lookup"><span data-stu-id="d8337-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="d8337-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-137"></span></span>

<span data-ttu-id="d8337-138">Existentes controles ActiveX de 32 bits, no son compatibles con las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="d8337-139">Para los controles ActiveX y los objetos COM:</span><span class="sxs-lookup"><span data-stu-id="d8337-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="d8337-140">Si dispone del código fuente, generar una versión de 64 bits usted mismo.</span><span class="sxs-lookup"><span data-stu-id="d8337-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="d8337-141">Si no dispone del código fuente, póngase en contacto con el proveedor para obtener una versión actualizada.</span><span class="sxs-lookup"><span data-stu-id="d8337-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="d8337-142">Procesos de 64 bits nativos de Office no pueden cargar los archivos binarios de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="d8337-143">Esto incluye los controles comunes de **MSComCtl** (TabStrip, la barra de herramientas, barra de estado, ProgressBar, TreeView, controles ListView por, ImageList, control deslizante, ImageComboBox) y los controles de **MSComCt2** (animación, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="d8337-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="d8337-144">Estos controles se instalaron con versiones de 32 bits de Office anteriores a Office 2010.</span><span class="sxs-lookup"><span data-stu-id="d8337-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="d8337-145">Debe encontrar una alternativa para las soluciones VBA existentes que usan estos controles al migrar el código a las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="d8337-146">Compatibilidad de API</span><span class="sxs-lookup"><span data-stu-id="d8337-146">API compatibility</span></span>
<span data-ttu-id="d8337-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-147"></span></span>

<span data-ttu-id="d8337-148">La combinación de las bibliotecas de VBA y tipo le ofrece una gran cantidad de funcionalidad para crear aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="d8337-149">Sin embargo, en ocasiones, se debe comunicar directamente con el sistema operativo y otros componentes, por ejemplo, al administrar memoria o procesos, cuando se trabaja con controles y ventanas de linke de elementos de la interfaz de usuario, o cuando se modifica el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="d8337-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="d8337-150">En estos escenarios, la mejor opción es utilizar una de las funciones externas que están incrustadas en archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="d8337-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="d8337-151">Puede hacerlo en VBA mediante la realización de llamadas a API utilizando instrucciones **Declare** .</span><span class="sxs-lookup"><span data-stu-id="d8337-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d8337-152">Microsoft proporciona un archivo Win32API.txt que contiene las instrucciones Declare 1.500 y una herramienta para copiar la instrucción **Declare** que desee en el código.</span><span class="sxs-lookup"><span data-stu-id="d8337-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="d8337-153">Sin embargo, estas instrucciones son para sistemas de 32 bits y se debe convertir a 64 bits mediante el uso de la información que se trata más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="d8337-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="d8337-154">Las instrucciones **Declare** existentes no se compilan en VBA de 64 bits hasta que haya marcado como seguros para 64 bits mediante el atributo **PtrSafe** .</span><span class="sxs-lookup"><span data-stu-id="d8337-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="d8337-155">Puede encontrar ejemplos de este tipo de conversión en el sitio Web del Excel MVP Jan Karel Pieterse en [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="d8337-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="d8337-156">La [Guía de usuario del Inspector de compatibilidad de código de Office](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) es una herramienta muy útil para inspeccionar la sintaxis de instrucciones **Declare** de API para el atributo **PtrSafe** , si es necesario, y el correspondiente tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d8337-156">The [Office Code Compatibility Inspector user's guide](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="d8337-157">Instrucciones **Declare** se parecen a uno de los siguientes, dependiendo de si se está llamando a una subrutina (que no tiene ningún valor devuelto) o una función (que tiene un valor devuelto).</span><span class="sxs-lookup"><span data-stu-id="d8337-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="d8337-158">La función de **nombre secundario** o **nombrefunción** se ha reemplazado por el nombre real del procedimiento en el archivo DLL y representa el nombre que se usa cuando se llama al procedimiento desde el código VBA.</span><span class="sxs-lookup"><span data-stu-id="d8337-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="d8337-159">También puede especificar un argumento **nombreAlias** para el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d8337-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="d8337-160">El nombre del archivo DLL que contiene el procedimiento que se llama sigue la palabra clave **Lib** .</span><span class="sxs-lookup"><span data-stu-id="d8337-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="d8337-161">Y, por último, la lista de argumentos contiene los parámetros y los tipos de datos que se deben pasar al procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d8337-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="d8337-162">La instrucción **Declare** siguiente abre una *subclave* en el registro de Windows y reemplaza su valor.</span><span class="sxs-lookup"><span data-stu-id="d8337-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="d8337-163">La entrada de Windows.h (identificador de ventana) para la función **RegOpenKeyA** es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8337-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="d8337-164">En Visual C y Microsoft Visual C++, en el ejemplo anterior se compila correctamente para 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="d8337-165">Esto es debido a que HKEY se define como un puntero, cuyo tamaño refleja el tamaño de la memoria de la plataforma que el código se compila en.</span><span class="sxs-lookup"><span data-stu-id="d8337-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="d8337-166">En versiones anteriores de VBA, se ha producido ningún tipo de datos de puntero específicos por lo que se usó el tipo de datos **Long** .</span><span class="sxs-lookup"><span data-stu-id="d8337-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="d8337-167">Y debido a que el tipo de datos **Long** es siempre este saltos cuando se usa en un sistema con memoria de 64 bits porque los superiores 32 bits se pueden truncar o es posible que sobrescribir otras direcciones de memoria de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="d8337-168">Cualquiera de estas situaciones puede provocar bloqueos imprevisibles de comportamiento o del sistema.</span><span class="sxs-lookup"><span data-stu-id="d8337-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="d8337-169">Para resolver este problema, VBA incluye un tipo de datos es true *puntero* : **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d8337-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="d8337-170">Este nuevo tipo de datos le permite escribir la instrucción **Declare** original correctamente como:</span><span class="sxs-lookup"><span data-stu-id="d8337-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="d8337-171">Este tipo de datos y el nuevo atributo **PtrSafe** permiten utilizar esta instrucción **Declare** en sistemas de 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="d8337-172">El atributo **PtrSafe** indica que el compilador VBA que la instrucción **Declare** está destinada a la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="d8337-173">Sin este atributo, el uso de la instrucción **Declare** en un sistema de 64 bits, se producirá un error en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="d8337-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="d8337-174">El atributo **PtrSafe** es opcional en la versión de 32 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="d8337-175">Esto permite que las instrucciones **Declare** existentes para que funcione como siempre lo han.</span><span class="sxs-lookup"><span data-stu-id="d8337-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="d8337-176">En la siguiente tabla se proporciona más información acerca del nuevo calificador y datos typeas así como otro tipo de datos, dos operadores de conversión y tres funciones.</span><span class="sxs-lookup"><span data-stu-id="d8337-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="d8337-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8337-177">Type</span></span>|<span data-ttu-id="d8337-178">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8337-178">Item</span></span>|<span data-ttu-id="d8337-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8337-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8337-180">Calificador</span><span class="sxs-lookup"><span data-stu-id="d8337-180">Qualifier</span></span>  <br/> |<span data-ttu-id="d8337-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="d8337-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="d8337-p119">Indica que la instrucción **Declare** es compatible con 64 bits. Este atributo es obligatorio en sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="d8337-184">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d8337-184">Data Type</span></span>  <br/> |<span data-ttu-id="d8337-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="d8337-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="d8337-186">Un tipo de datos de la variable que es un tipo de datos de 4 bytes en las versiones de 32 bits y un tipo de datos de 8 bytes en las versiones de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="d8337-187">Esta es la manera recomendada de declaración de un puntero o un identificador para el nuevo código, sino también para el código heredado si tiene que ejecutar en la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="d8337-188">Sólo se admite en el tiempo de ejecución de VBA 7 de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8337-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="d8337-189">Tenga en cuenta que puede asignar valores numéricos a ella pero tipos no numéricos.</span><span class="sxs-lookup"><span data-stu-id="d8337-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="d8337-190">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d8337-190">Data Type</span></span>  <br/> |<span data-ttu-id="d8337-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="d8337-191">**LongLong**</span></span> <br/> |<span data-ttu-id="d8337-192">Este es un tipo de datos de 8 bytes que sólo está disponible en versiones de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="d8337-193">Puede asignar valores numéricos pero tipos no numéricos (para evitar el truncamiento).</span><span class="sxs-lookup"><span data-stu-id="d8337-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="d8337-194">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="d8337-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="d8337-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="d8337-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="d8337-196">Convierte una expresión simple en un tipo de datos **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d8337-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="d8337-197">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="d8337-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="d8337-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="d8337-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="d8337-199">Convierte una expresión simple en un tipo de datos **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="d8337-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="d8337-200">Funci?n</span><span class="sxs-lookup"><span data-stu-id="d8337-200">Function</span></span>  <br/> |<span data-ttu-id="d8337-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="d8337-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="d8337-p122">Convertidor de datos Variant. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="d8337-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="d8337-204">Funci?n</span><span class="sxs-lookup"><span data-stu-id="d8337-204">Function</span></span>  <br/> |<span data-ttu-id="d8337-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="d8337-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="d8337-p123">Convertidor de objetos. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="d8337-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="d8337-208">Funci?n</span><span class="sxs-lookup"><span data-stu-id="d8337-208">Function</span></span>  <br/> |<span data-ttu-id="d8337-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="d8337-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="d8337-p124">Convertidor de cadena. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="d8337-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="d8337-212">El siguiente ejemplo muestra cómo usar algunos de estos elementos en una instrucción **Declare**.</span><span class="sxs-lookup"><span data-stu-id="d8337-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="d8337-213">Tenga en cuenta las instrucciones **Declare** sin el atributo **PtrSafe** se supone que no sea compatible con la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="d8337-214">Hay dos constantes de compilación condicional: **VBA7** y **Win64**.</span><span class="sxs-lookup"><span data-stu-id="d8337-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="d8337-215">Para garantizar la compatibilidad con versiones anteriores con versiones anteriores de Microsoft Office, utiliza la constante de **VBA7** (Esto es el caso más típico) para evitar que el código de 64 bits que se usa en la versión anterior de Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="d8337-216">Para que el código sea diferente entre la versión de 32 bits y la versión de 64 bits, como una llamada a un coprocesador API que usa **LongLong** para su versión de 64 bits y **largo** para su versión de 32 bits, utilice la constante **Win64** .</span><span class="sxs-lookup"><span data-stu-id="d8337-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="d8337-217">El siguiente código muestra el uso de estas dos constantes.</span><span class="sxs-lookup"><span data-stu-id="d8337-217">The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="d8337-218">En resumen, si escribir código de 64 bits y va a utilizar en las versiones anteriores de Office, que desea usar la constante de compilación condicional **VBA7** .</span><span class="sxs-lookup"><span data-stu-id="d8337-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="d8337-219">Sin embargo, si escribe un código de 32 bits en Office, ese código funciona como se encuentra en las versiones anteriores de Office sin necesidad de la constante de compilación.</span><span class="sxs-lookup"><span data-stu-id="d8337-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="d8337-220">Si desea asegurarse de que está utilizando instrucciones de 32 bits para las versiones de 32 bits y 64 bits de instrucciones para las versiones de 64 bits, la mejor opción es usar la constante de compilación condicional **Win64** .</span><span class="sxs-lookup"><span data-stu-id="d8337-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="d8337-221">Uso de atributos de compilación condicional</span><span class="sxs-lookup"><span data-stu-id="d8337-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="d8337-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-222"></span></span>

<span data-ttu-id="d8337-223">En el ejemplo siguiente se muestra el código de VBA escrito para 32 bits que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="d8337-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="d8337-224">Tenga en cuenta los tipos de datos en el código heredado que se actualizan para utilizar **LongPtr** , ya que hacen referencia a punteros o identificadores.</span><span class="sxs-lookup"><span data-stu-id="d8337-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="d8337-225">Código de VBA escrito para versiones de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d8337-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="d8337-226">Código VBA que se modificó para versiones de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d8337-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="d8337-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d8337-228">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="d8337-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="d8337-229">¿Cuándo debo usar la versión de 64 bits de Office?</span><span class="sxs-lookup"><span data-stu-id="d8337-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="d8337-230">Esto es más una cuestión de la aplicación host (Excel, Word etc.) que está utilizando.</span><span class="sxs-lookup"><span data-stu-id="d8337-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="d8337-231">Por ejemplo, Excel es capaz de controlar mucho más grandes hojas de cálculo con la versión de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d8337-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="d8337-232">¿Puedo instalar versiones de 32 bits y de 64 bits de Office en paralelo?</span><span class="sxs-lookup"><span data-stu-id="d8337-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="d8337-233">No.</span><span class="sxs-lookup"><span data-stu-id="d8337-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="d8337-234">¿Cuándo debo convertir parámetros largos a LongPtr?</span><span class="sxs-lookup"><span data-stu-id="d8337-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="d8337-235">Debe consultar la documentación de API de Windows en la red de programadores de Microsoft para la función que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="d8337-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="d8337-236">Punteros y controladores necesitan que se va a convertir a **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d8337-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="d8337-237">Por ejemplo, la documentación de [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) proporciona la siguiente firma:</span><span class="sxs-lookup"><span data-stu-id="d8337-237">As an example, the documentation for [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="d8337-238">Los parámetros se definen como:</span><span class="sxs-lookup"><span data-stu-id="d8337-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="d8337-239">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d8337-239">Parameter</span></span>|<span data-ttu-id="d8337-240">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8337-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8337-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="d8337-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="d8337-242">*Controlar* a una clave del registro abierta.</span><span class="sxs-lookup"><span data-stu-id="d8337-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="d8337-243">lpSubKey [entrada, opcional]</span><span class="sxs-lookup"><span data-stu-id="d8337-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="d8337-244">El nombre de la subclave del registro que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="d8337-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="d8337-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="d8337-245">ulOptions</span></span>  <br/> |<span data-ttu-id="d8337-246">Este parámetro está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d8337-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="d8337-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="d8337-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="d8337-248">Máscara que especifica los derechos de acceso que desee a la clave.</span><span class="sxs-lookup"><span data-stu-id="d8337-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="d8337-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="d8337-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="d8337-250">Un *puntero* a una variable que recibe un identificador de la clave abierta.</span><span class="sxs-lookup"><span data-stu-id="d8337-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="d8337-251">En [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), la instrucción **Declare** se define como:</span><span class="sxs-lookup"><span data-stu-id="d8337-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="d8337-252">¿Debo convertir punteros e identificadores en estructuras?</span><span class="sxs-lookup"><span data-stu-id="d8337-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="d8337-253">Sí.</span><span class="sxs-lookup"><span data-stu-id="d8337-253">Yes.</span></span> <span data-ttu-id="d8337-254">Vea el tipo de **mensaje** en Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="d8337-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="d8337-255">¿Cuándo debo usar strptr, varpt y objptr?</span><span class="sxs-lookup"><span data-stu-id="d8337-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="d8337-256">Debe utilizar estas funciones para recuperar punteros a cadenas, variables y objetos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d8337-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="d8337-257">En la versión de 64 bits de Office, estas funciones devolverán de 64 bits **LongPtr**, que se puede pasar a las instrucciones **Declare** .</span><span class="sxs-lookup"><span data-stu-id="d8337-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="d8337-258">El uso de estas funciones no ha cambiado desde las versiones anteriores de VBA.</span><span class="sxs-lookup"><span data-stu-id="d8337-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="d8337-259">La única diferencia es que ahora devuelven un **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d8337-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8337-260">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8337-260">See also</span></span>
<span data-ttu-id="d8337-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="d8337-261"></span></span>

- [<span data-ttu-id="d8337-262">Anatomía de una instrucción Declare</span><span class="sxs-lookup"><span data-stu-id="d8337-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

