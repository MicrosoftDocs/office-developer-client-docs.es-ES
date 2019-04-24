---
title: Compatibilidad entre versiones de 32 y 64 bits de Office
ms.date: 04/27/2016
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra cómo la versión de 32 bits de Office es compatible con de 64 bits.
localization_priority: Priority
ms.openlocfilehash: b03323b37b242c9992c47cd737ae54f3f9bbf2ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359825"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="dee91-103">Compatibilidad entre versiones de 32 y 64 bits de Office</span><span class="sxs-lookup"><span data-stu-id="dee91-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="dee91-104">Descubra cómo la versión de 32 bits de Office es compatible con de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="dee91-105">Las aplicaciones de Office están disponibles en versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="dee91-106">Las versiones de 64 bits de Office permiten desplazar más datos para obtener una mayor capacidad, por ejemplo, al trabajar con números grandes en Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="dee91-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="dee91-107">Al escribir código de 32 bits, puede usar la versión de 64 bits de Office sin cambios.</span><span class="sxs-lookup"><span data-stu-id="dee91-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="dee91-108">Sin embargo, al escribir el código de 64 bits, debe asegurarse de que el código contiene palabras clave específicas y constantes de compilación condicional para asegurarse de que el código es compatible con la versión anterior de Office y que el código correcto se ejecuta si se combinan códigos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="dee91-109">Visual Basic para Aplicaciones 7.0 (VBA 7) se publicó en las versiones de 64 bits de Office y funciona tanto con aplicaciones de 32 como de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="dee91-110">Los cambios descritos en este artículo solo se aplican a las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="dee91-111">Usar las versiones de 32 bits de Microsoft Office le permite utilizar soluciones integradas en versiones anteriores de Office sin realizar modificaciones.</span><span class="sxs-lookup"><span data-stu-id="dee91-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dee91-112">De forma predeterminada, cuando se instala una versión de 64 bits de Office, también se instala la versión de 32 bits con el sistema de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="dee91-113">Debe seleccionar explícitamente la opción de instalación de la versión de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="dee91-114">En VBA 7, se deben actualizar las instrucciones existentes de la API de Windows (instrucciones **Declarar**) para que funcione con la versión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="dee91-115">Además, se deben actualizar los punteros de dirección y los controladores de ventanas en los tipos definidos por el usuario que usan estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="dee91-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="dee91-116">Esto se describe en detalle en este artículo, así como también los problemas de compatibilidad entre las versiones de 32 y 64 bits y las soluciones recomendadas.</span><span class="sxs-lookup"><span data-stu-id="dee91-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="dee91-117">Comparación de los sistemas de 32 y 64 bits</span><span class="sxs-lookup"><span data-stu-id="dee91-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="dee91-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-118"></span></span>

<span data-ttu-id="dee91-119">Las aplicaciones integradas con las versiones de 64 bits de Office pueden hacer referencia a espacios de direcciones más grandes que las versiones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="dee91-120">Esto significa que puede usar más memoria física para datos que antes, lo que probablemente reduzca la sobrecarga utilizada en la entrada y salida de datos de la memoria física</span><span class="sxs-lookup"><span data-stu-id="dee91-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="dee91-121">Además de hacer referencia a ubicaciones específicas (denominadas punteros) en la memoria física, también puede usar direcciones para hacer referencia a los identificadores de ventanas (denominados controladores).</span><span class="sxs-lookup"><span data-stu-id="dee91-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="dee91-122">El tamaño (en bytes) del puntero o controlador depende de si usa un sistema de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="dee91-123">Si desea ejecutar las soluciones existentes con las versiones de 64 bits de Office, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="dee91-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="dee91-124">Los procesos nativos de 64 bits de Office no pueden cargar archivos binarios de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="dee91-125">Este será un problema habitual cuando se tengan ya controles Microsoft ActiveX y complementos.</span><span class="sxs-lookup"><span data-stu-id="dee91-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="dee91-126">Anteriormente, VBA no tenía un tipo de datos de punteros, por lo que se tenían que usar variables de 32 bits para almacenar punteros y controladores.</span><span class="sxs-lookup"><span data-stu-id="dee91-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="dee91-127">Ahora, estas variables truncan los valores de 64 bits devueltos por las llamadas a la API al usar instrucciones **Declarar**.</span><span class="sxs-lookup"><span data-stu-id="dee91-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="dee91-128">Base del código de VBA 7</span><span class="sxs-lookup"><span data-stu-id="dee91-128">VBA 7 code base</span></span>
<span data-ttu-id="dee91-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-129"></span></span>

<span data-ttu-id="dee91-130">VBA 7 reemplaza la base del código VBA en Office 2007 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="dee91-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="dee91-131">VBA 7 se encuentra disponible tanto en la versión de 32 como en la de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="dee91-132">Ofrece dos constantes de compilación condicional:</span><span class="sxs-lookup"><span data-stu-id="dee91-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="dee91-133">**VBA7**: ayuda a garantizar la compatibilidad con versiones anteriores del código al comprobar si la aplicación usa VBA 7 o la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="dee91-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="dee91-134">**Win64**: comprueba si el código se ejecuta en 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="dee91-135">Con algunas excepciones, las macros de un documento que funcionan en la versión de 32 bits de la aplicación también funcionan en la versión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="dee91-136">Compatibilidad de controles ActiveX y complementos COM</span><span class="sxs-lookup"><span data-stu-id="dee91-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="dee91-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-137"></span></span>

<span data-ttu-id="dee91-138">Los controles ActiveX de 32 bits existentes no son compatibles con las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="dee91-139">Para controles ActiveX y objetos COM:</span><span class="sxs-lookup"><span data-stu-id="dee91-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="dee91-140">Si se dispone del código fuente, puede generar una versión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="dee91-141">Si no cuenta con el código fuente, póngase en contacto con el proveedor para obtener una versión actualizada.</span><span class="sxs-lookup"><span data-stu-id="dee91-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="dee91-142">Los procesos nativos de 64 bits de Office no pueden cargar archivos binarios de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="dee91-143">Esto incluye los controles comunes de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) y los controles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="dee91-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="dee91-144">Estos controles se instalaron con versiones de 32 bits de Office anteriores a Office 2010.</span><span class="sxs-lookup"><span data-stu-id="dee91-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="dee91-145">Deberá buscar una alternativa para las soluciones de VBA existentes que usan estos controles al migrar el código a las versiones de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="dee91-146">Compatibilidad de API</span><span class="sxs-lookup"><span data-stu-id="dee91-146">API compatibility</span></span>
<span data-ttu-id="dee91-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-147"></span></span>

<span data-ttu-id="dee91-148">La combinación de las bibliotecas de VBA y de tipos ofrece una gran variedad de funcionalidad para crear aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="dee91-149">Sin embargo, a veces debe comunicarse directamente con el sistema operativo y otros componentes, como cuando administra la memoria o los procesos al trabajar con elementos de la interfaz de usuario, tales como controles y ventanas o cuando se modifica el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="dee91-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="dee91-150">En estos casos, la mejor opción es usar una de las funciones externas incrustadas en archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="dee91-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="dee91-151">Para ello en VBA, realice llamadas a la API con instrucciones **Declarar**.</span><span class="sxs-lookup"><span data-stu-id="dee91-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dee91-152">Microsoft proporciona un archivo Win32API.txt con 1 500 instrucciones **Declarar** y una herramienta para copiar la que desee en el código.</span><span class="sxs-lookup"><span data-stu-id="dee91-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="dee91-153">Sin embargo, estas instrucciones son para sistemas de 32 bits y deben convertirse a 64 bits con la información que se describe más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="dee91-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="dee91-154">Las instrucciones **Declarar** existentes no se compilarán en VBA de 64 bits hasta que hayan sido marcadas como seguras para 64 bits a través del atributo **PtrSafe**.</span><span class="sxs-lookup"><span data-stu-id="dee91-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="dee91-155">Encontrará ejemplos de este tipo de conversión en el sitio web de Jan Karel Pieterse [ https://www.jkp-ads.com/articles/apideclarations.asp ](https://www.jkp-ads.com/articles/apideclarations.asp)sobre Excel MVP.</span><span class="sxs-lookup"><span data-stu-id="dee91-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="dee91-156">La [Guía del usuario de Office Code Compatibility Inspector](https://technet.microsoft.com/es-ES/library/ee833946%28office.14%29.aspx) es una herramienta útil para inspeccionar la sintaxis de las instrucciones **Declarar** de la API para el atributo **PtrSafe**, si es necesario, y el tipo de valor devuelto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dee91-156">The [Office Code Compatibility Inspector user's guide](https://technet.microsoft.com/es-ES/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="dee91-157">Las instrucciones **Declarar** se verán como algunas de las siguientes, dependiendo de si se llama a una subrutina (que no tiene valor devuelto) o a una función (que sí tiene un valor devuelto).</span><span class="sxs-lookup"><span data-stu-id="dee91-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="dee91-158">La función **SubName** o **FunctionName** se reemplaza por el nombre real del procedimiento en el archivo DLL y representa el nombre que se usa cuando se llama al procedimiento desde el código de VBA.</span><span class="sxs-lookup"><span data-stu-id="dee91-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="dee91-159">También puede especificar un argumento **AliasName** para el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="dee91-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="dee91-160">El nombre del archivo DLL que contiene el procedimiento al que se llama se coloca a continuación de la palabra clave **Lib**.</span><span class="sxs-lookup"><span data-stu-id="dee91-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="dee91-161">Y por último, la lista de argumentos contiene los parámetros y los tipos de datos que se deben pasar al procedimiento.</span><span class="sxs-lookup"><span data-stu-id="dee91-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="dee91-162">La siguiente instrucción **Declarar** abre una *subclave* en el registro de Windows y reemplaza su valor.</span><span class="sxs-lookup"><span data-stu-id="dee91-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="dee91-163">La entrada Windows.h (controlador de la ventana) de la función **RegOpenKeyA** es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="dee91-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="dee91-164">En Visual C y Microsoft Visual C++, el ejemplo anterior compila correctamente tanto para 32 como para 64-bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="dee91-165">Esto es porque HKEY está definido como un puntero, cuyo tamaño refleja el tamaño de la memoria de la plataforma en la que se compila el código.</span><span class="sxs-lookup"><span data-stu-id="dee91-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="dee91-166">En versiones anteriores de VBA, no había ningún tipo de datos específico del puntero así que se utilizó el tipo de datos **Long**.</span><span class="sxs-lookup"><span data-stu-id="dee91-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="dee91-167">Además, dado que el tipo de datos **Long** siempre es de 32 bits, este se interrumpe cuando se utiliza en un sistema con memoria de 64 bits ya que los 32 bits superiores pueden truncarse o podrían sobrescribir otras direcciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="dee91-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="dee91-168">Cualquiera de estas situaciones puede causar comportamientos impredecibles o bloqueos del sistema.</span><span class="sxs-lookup"><span data-stu-id="dee91-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="dee91-169">Para resolver esto, VBA incluye un verdadero tipo de datos *puntero*: **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="dee91-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="dee91-170">Este nuevo tipo de datos le permite escribir la instrucción **Declarar** original correctamente como:</span><span class="sxs-lookup"><span data-stu-id="dee91-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="dee91-171">Este tipo de datos y el nuevo atributo **PtrSafe** le permiten utilizar esta instrucción **Declarar** en sistemas de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="dee91-172">El atributo **PtrSafe** le indica al compilador de VBA que la instrucción **Declarar** está destinada a la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="dee91-173">Sin este atributo, al usar la instrucción **Declarar** en un sistema de 64 bits se producirá un error en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="dee91-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="dee91-174">El atributo **PtrSafe** es opcional, en la versión de 32 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="dee91-175">Esto permite que las instrucciones **Declarar** existentes funcionen de manera habitual.</span><span class="sxs-lookup"><span data-stu-id="dee91-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="dee91-176">La siguiente tabla proporciona más información sobre el nuevo calificador y el tipo de datos, así como otro tipo de datos, dos operadores de conversión y tres funciones.</span><span class="sxs-lookup"><span data-stu-id="dee91-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="dee91-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="dee91-177">Type</span></span>|<span data-ttu-id="dee91-178">Item</span><span class="sxs-lookup"><span data-stu-id="dee91-178">Item</span></span>|<span data-ttu-id="dee91-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="dee91-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dee91-180">Calificador</span><span class="sxs-lookup"><span data-stu-id="dee91-180">Qualifier</span></span>  <br/> |<span data-ttu-id="dee91-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="dee91-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="dee91-p119">Indica que la instrucción **Declarar** es compatible con 64 bits. Este atributo es obligatorio en sistemas de 64 bits.  </span><span class="sxs-lookup"><span data-stu-id="dee91-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="dee91-184">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dee91-184">Data Type</span></span>  <br/> |<span data-ttu-id="dee91-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="dee91-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="dee91-186">Un tipo de datos variable que es un tipo de datos de 4 bytes en versiones de 32 bits y un tipo de datos de 8 bytes en versiones de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="dee91-187">Esta es la manera recomendada de declarar un puntero o un controlador para un código nuevo, pero también para el código heredado si se tiene que ejecutar en la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="dee91-188">Solo es compatible en el tiempo de ejecución de VBA 7 de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dee91-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="dee91-189">Tenga en cuenta que puede asignarle valores numéricos, pero no tipos numéricos.</span><span class="sxs-lookup"><span data-stu-id="dee91-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="dee91-190">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dee91-190">Data Type</span></span>  <br/> |<span data-ttu-id="dee91-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="dee91-191">**LongLong**</span></span> <br/> |<span data-ttu-id="dee91-192">Este es un tipo de datos de 8 bytes que solo está disponible en versiones de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="dee91-193">Puede asignar valores numéricos, pero no tipos numéricos (para evitar truncamiento).</span><span class="sxs-lookup"><span data-stu-id="dee91-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="dee91-194">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="dee91-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="dee91-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="dee91-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="dee91-196">Convierte una expresión sencilla en un tipo de datos **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="dee91-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="dee91-197">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="dee91-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="dee91-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="dee91-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="dee91-199">Convierte una expresión sencilla en un tipo de datos **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="dee91-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="dee91-200">Función</span><span class="sxs-lookup"><span data-stu-id="dee91-200">Function</span></span>  <br/> |<span data-ttu-id="dee91-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="dee91-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="dee91-p122">Convertidor Variant. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="dee91-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="dee91-204">Función</span><span class="sxs-lookup"><span data-stu-id="dee91-204">Function</span></span>  <br/> |<span data-ttu-id="dee91-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="dee91-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="dee91-p123">Convertidor Object. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="dee91-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="dee91-208">Función</span><span class="sxs-lookup"><span data-stu-id="dee91-208">Function</span></span>  <br/> |<span data-ttu-id="dee91-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="dee91-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="dee91-p124">Convertidor String. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="dee91-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="dee91-212">El siguiente ejemplo muestra cómo usar algunos de estos elementos en una instrucción **Declarar**.</span><span class="sxs-lookup"><span data-stu-id="dee91-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="dee91-213">Tenga en cuenta que se asume que las instrucciones **Declarar** sin el atributo **PtrSafe** no son compatibles con la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="dee91-214">Existen dos constantes de compilación condicional: **VBA7** y **Win64**.</span><span class="sxs-lookup"><span data-stu-id="dee91-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="dee91-215">Para garantizar la compatibilidad con versiones anteriores de Microsoft Office, se utiliza la constante **VBA7** (esto es lo más habitual) para evitar que el código de 64 bits se use en la versión anterior de Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="dee91-216">Para todo código que sea diferente de la versión de 32 y la de 64 bits, como por ejemplo, llamar a una API de matemáticas que utiliza **LongLong** para su versión de 64 bits y **Long** para su versión de 32 bits, se usa la constante **Win64**.</span><span class="sxs-lookup"><span data-stu-id="dee91-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="dee91-217">El siguiente código muestra el uso de estas dos constantes.</span><span class="sxs-lookup"><span data-stu-id="dee91-217">The following code shows the use of these two constants.</span></span> 
  
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

<span data-ttu-id="dee91-218">En resumen, si escribe código de 64 bits y desea usarlo en versiones anteriores de Office, tendrá que usar la constante de compilación condicional **VBA7**.</span><span class="sxs-lookup"><span data-stu-id="dee91-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="dee91-219">Sin embargo, si escribe código de 32 bits en Office, ese código funciona como en versiones anteriores de Office sin necesidad de usar la constante de compilación.</span><span class="sxs-lookup"><span data-stu-id="dee91-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="dee91-220">Si desea asegurarse de que está usando instrucciones de 32 bits para versiones de 32 bits e instrucciones de 64 bits para versiones de 64 bits, la mejor opción es usar la constante de compilación condicional **Win64**.</span><span class="sxs-lookup"><span data-stu-id="dee91-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="dee91-221">Uso de atributos de compilación condicional</span><span class="sxs-lookup"><span data-stu-id="dee91-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="dee91-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-222"></span></span>

<span data-ttu-id="dee91-223">El siguiente ejemplo muestra el código VBA escrito para 32 bits que debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="dee91-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="dee91-224">Observe los tipos de datos en el código heredado que se actualizan para usar **LongPtr** ya que hacen referencia a punteros o controladores.</span><span class="sxs-lookup"><span data-stu-id="dee91-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="dee91-225">Código VBA escrito para versiones de 32 bits</span><span class="sxs-lookup"><span data-stu-id="dee91-225">VBA code written for 32-bit versions</span></span>
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="dee91-226">Código VBA reescrito para versiones de 64 bits</span><span class="sxs-lookup"><span data-stu-id="dee91-226">VBA code rewritten for 64-bit versions</span></span>
  
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

<span data-ttu-id="dee91-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="dee91-228">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="dee91-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="dee91-229">¿Cuándo debería usar la versión de 64 bits de Office?</span><span class="sxs-lookup"><span data-stu-id="dee91-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="dee91-230">Depende, en gran medida, de la aplicación host (Word, Excel, etc.) que utiliza.</span><span class="sxs-lookup"><span data-stu-id="dee91-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="dee91-231">Por ejemplo, Excel es capaz de manejar hojas de cálculo mucho más grandes con la versión de 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dee91-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="dee91-232">¿Puedo instalar las versiones de 32 y 64 bits de Office en paralelo?</span><span class="sxs-lookup"><span data-stu-id="dee91-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="dee91-233">No.</span><span class="sxs-lookup"><span data-stu-id="dee91-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="dee91-234">¿Cuándo debo convertir los parámetros Long a LongPtr?</span><span class="sxs-lookup"><span data-stu-id="dee91-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="dee91-235">Debe comprobar la documentación de la API de Windows en Microsoft Developers Network para la función que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="dee91-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="dee91-236">Es necesario convertir los controladores y punteros a **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="dee91-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="dee91-237">Por ejemplo, la documentación de [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) proporciona la siguiente firma:</span><span class="sxs-lookup"><span data-stu-id="dee91-237">As an example, the documentation for [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="dee91-238">Los parámetros se definen como:</span><span class="sxs-lookup"><span data-stu-id="dee91-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="dee91-239">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dee91-239">Parameter</span></span>|<span data-ttu-id="dee91-240">Descripción</span><span class="sxs-lookup"><span data-stu-id="dee91-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dee91-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="dee91-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="dee91-242">Un *controlador* a una clave del registro abierta.</span><span class="sxs-lookup"><span data-stu-id="dee91-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="dee91-243">lpSubKey [in, opcional]</span><span class="sxs-lookup"><span data-stu-id="dee91-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="dee91-244">El nombre de la subclave del registro que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="dee91-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="dee91-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="dee91-245">ulOptions</span></span>  <br/> |<span data-ttu-id="dee91-246">Este parámetro está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dee91-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="dee91-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="dee91-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="dee91-248">Máscara que especifica los derechos de acceso deseados a la clave.</span><span class="sxs-lookup"><span data-stu-id="dee91-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="dee91-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="dee91-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="dee91-250">Un *puntero* a una variable que recibe un controlador a la clave abierta.</span><span class="sxs-lookup"><span data-stu-id="dee91-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="dee91-251">En [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), la instrucción **Declarar** se define como:</span><span class="sxs-lookup"><span data-stu-id="dee91-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="dee91-252">¿Debo convertir punteros y controladores en estructuras?</span><span class="sxs-lookup"><span data-stu-id="dee91-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="dee91-253">Sí.</span><span class="sxs-lookup"><span data-stu-id="dee91-253">Yes.</span></span> <span data-ttu-id="dee91-254">Consulte el tipo **MSG** en Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="dee91-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="dee91-255">¿Cuándo debo usar strptr, varpt y objptr?</span><span class="sxs-lookup"><span data-stu-id="dee91-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="dee91-256">Debe usar estas funciones para recuperar punteros a cadenas, variables y objetos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dee91-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="dee91-257">En la versión de 64 bits de Office, estas funciones devuelven un parámetro **LongPtr** de 64 bits, que se puede pasar a las instrucciones **Declarar**.</span><span class="sxs-lookup"><span data-stu-id="dee91-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="dee91-258">El uso de estas funciones no ha cambiado de versiones anteriores de VBA.</span><span class="sxs-lookup"><span data-stu-id="dee91-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="dee91-259">La única diferencia es que ahora devuelven un parámetro **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="dee91-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dee91-260">Vea también</span><span class="sxs-lookup"><span data-stu-id="dee91-260">See also</span></span>
<span data-ttu-id="dee91-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="dee91-261"></span></span>

- [<span data-ttu-id="dee91-262">Componentes de la Instrucción Declarar</span><span class="sxs-lookup"><span data-stu-id="dee91-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

