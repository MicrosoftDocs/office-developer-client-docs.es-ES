---
title: Obtener acceso a DLL en Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- acceder a dll [excel 2007], DLL [Excel 2007], acceder en Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815638"
---
# <a name="access-dlls-in-excel"></a><span data-ttu-id="c9a8e-104">Obtener acceso a DLL en Excel</span><span class="sxs-lookup"><span data-stu-id="c9a8e-104">How to: Access DLLs in Excel</span></span>

<span data-ttu-id="c9a8e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c9a8e-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c9a8e-106">Puede obtener acceso a una función DLL o comando en Microsoft Excel de varias formas:</span><span class="sxs-lookup"><span data-stu-id="c9a8e-106">You can access a DLL function or command in Microsoft Excel in several ways:</span></span>
  
- <span data-ttu-id="c9a8e-107">A trav�s del m�dulo de códigoMicrosoft Visual Basic para aplicaciones (VBA) en el que la función o el comando est� disponible mediante una instrucci�n **Declare**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-107">Through a Microsoft Visual Basic for Applications (VBA) code module in which the function or command has been made available using a **Declare** statement.</span></span> 
    
- <span data-ttu-id="c9a8e-108">A trav�s de una hoja de macros XLM con las funciones **CALL** o **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-108">Through an XLM macro sheet by using the **CALL** or **REGISTER** functions.</span></span> 
    
- <span data-ttu-id="c9a8e-109">Directamente desde la hoja de cálculo o de un elemento personalizado de la interfaz de usuario (IU).</span><span class="sxs-lookup"><span data-stu-id="c9a8e-109">Directly from the worksheet or from a customized item in the user interface (UI).</span></span>
    
<span data-ttu-id="c9a8e-p101">Esta documentaci�n no trata las funciones XLM. Se recomienda que use uno de los dos enfoques.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p101">This documentation does not cover XLM functions. It is recommended that you use either of the other two approaches.</span></span>
  
<span data-ttu-id="c9a8e-p102">Para acceder directamente desde la hoja de cálculo o desde un elemento personalizado de la interfaz de usuario, la función o el comando se debe registrar primero con Excel. Para obtener información sobre el registro de comandos y funciones, consulte [Acceso al códigoXLL en Excel](accessing-xll-code-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p102">To be accessed directly from the worksheet or from a customized item in the UI, the function or command must first be registered with Excel. For information about registering commands and functions, see [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span></span>
  
## <a name="calling-dll-functions-and-commands-from-vba"></a><span data-ttu-id="c9a8e-114">Llamar a funciones y comandos DLL desde VBA</span><span class="sxs-lookup"><span data-stu-id="c9a8e-114">Calling DLL Functions and Commands from VBA</span></span>

<span data-ttu-id="c9a8e-p103">Puede acceder a funciones y comandos DLL de VBA con la instrucci�n **Declare**. Esta instrucci�n tiene una sintaxis para los comandos y otra para las funciones.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p103">You can access DLL functions and commands in VBA by using the **Declare** statement. This statement has one syntax for commands and one for functions.</span></span> 
  
- <span data-ttu-id="c9a8e-117">**Sintaxis 1: comandos**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-117">**Syntax 1 - commands**</span></span>
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- <span data-ttu-id="c9a8e-118">**Sintaxis 2: funciones**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-118">**Syntax 2 - functions**</span></span>
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

<span data-ttu-id="c9a8e-p104">Las palabras clave opcionales **Public** y **Private** especifican el �mbito de la función importada: todo el proyecto de Visual Basic o el m�dulo de Visual Basic, respectivamente. El nombre es el nombre que quiere usar en el códigoVBA. Si esto difiere del nombre del DLL, debe usar el especificador de Alias "aliasname" y proporcionar el nombre de la función como exportada por el DLL. Si quiere acceder a una función DLL por referencia para un n�mero ordinal DLL, debe proporcionar un nombre de alias, que es el ordinal con el prefijo **#**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p104">The optional **Public** and **Private** keywords specify the scope of the imported function: the entire Visual Basic project or just the Visual Basic module, respectively. The name is the name that you want to use in the VBA code. If this differs from the name in the DLL, you must use the Alias "aliasname" specifier, and you should give the name of the function as exported by the DLL. If you want to access a DLL function by reference to a DLL ordinal number, you must provide an alias name, which is the ordinal prefixed by **#**.</span></span>
  
<span data-ttu-id="c9a8e-p105">Los comandos deben devolver **void**. Las funciones deben devolver tipos que VBA pueda reconocer **ByVal**. Esto significa que algunos tipos se devuelven m�s f�cilmente modificando los argumentos locales: cadenas, matrices, tipos definidos por el usuario y objetos.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p105">Commands should return **void**. Functions should return types that VBA can recognize **ByVal**. This means that some types are more easily returned by modifying arguments in place: strings, arrays, user-defined types, and objects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c9a8e-p106">VBA no puede comprobar que la lista de argumentos y el retorno que se indica en el m�dulo de Visual Basic son los mismos seg�n la codificaci�n de DLL. Debe comprobar usted mismo con cuidado, ya que un error podr�a provocar el bloqueo de Excel.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p106">VBA cannot check that the argument list and return stated in the Visual Basic module are the same as coded in the DLL. You should check this yourself very carefully, because a mistake could cause Excel to crash.</span></span> 
  
<span data-ttu-id="c9a8e-p107">Cuando la referencia o el puntero no pasan los argumentos de la función o del comando, deben ir precedidos por la palabra clave **ByVal** en la declaraci�n **arglist**. Cuando una función de C o C++ toma argumentos de puntero o una función de C++ toma argumentos de referencia, deben pasar **ByRef**. La palabra clave **ByRef** se puede omitir de las listas de argumentos porque es el valor predeterminado en VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p107">When the function or command's arguments are not passed by reference or pointer, they must be preceded by the **ByVal** keyword in the **arglist** declaration. When a C/C++ function takes pointer arguments, or a C++ function takes reference arguments, they should be passed **ByRef**. The keyword **ByRef** can be omitted from argument lists because it is the default in VBA.</span></span> 
  
### <a name="argument-types-in-cc-and-vba"></a><span data-ttu-id="c9a8e-131">Tipos de argumento en C/C++ y VBA</span><span class="sxs-lookup"><span data-stu-id="c9a8e-131">Argument Types in C/C++ and VBA</span></span>

<span data-ttu-id="c9a8e-132">Debe tener en cuenta lo siguiente cuando se comparan las declaraciones de tipos de argumentos en C o C++ y VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-132">You should note the following when you compare the declarations of argument types in C/C++ and VBA.</span></span>
  
- <span data-ttu-id="c9a8e-133">Se pasa un **String** de VBA como un puntero a una estructura BSTR de cadena de bytes al pasar ByVal, y como un puntero a un puntero al pasar **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-133">A VBA **String** is passed as a pointer to a byte-string BSTR structure when passed ByVal, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="c9a8e-134">**Variant** de VBA que contiene una cadena se pasa como puntero a una estructura BSTR de cadena de caracteres anchos Unicode al pasar **ByVal**, y como un puntero a un puntero al pasar **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-134">A VBA **Variant** that contains a string is passed as a pointer to a Unicode wide-character string BSTR structure when passed **ByVal**, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="c9a8e-135">**Integer** de VBA es un tipo de 16 bits equivalente a un signed short en C/C++.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-135">The VBA **Integer** is a 16-bit type equivalent to a signed short in C/C++.</span></span> 
    
- <span data-ttu-id="c9a8e-136">**Long** de VBA es un tipo de 32 bits equivalente a un signed int en C/C++.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-136">The VBA **Long** is a 32-bit type equivalent to a signed int in C/C++.</span></span> 
    
- <span data-ttu-id="c9a8e-137">Tanto VBA como C/C++ permiten la definici�n de tipos de datos definidos por el usuario, con las instrucciones **Type** y **struct** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-137">Both VBA and C/C++ allow the definition of user-defined data types, using the **Type** and **struct** statements respectively.</span></span> 
    
- <span data-ttu-id="c9a8e-138">Tanto VBA como C/C++ admiten el tipo de datos **Variant**, definidos para C/C++ en los archivos de encabezado de Windows OLE/COM como VARIANT.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-138">Both VBA and C/C++ support the **Variant** data type, defined for C/C++ in the Windows OLE/COM header files as VARIANT.</span></span> 
    
- <span data-ttu-id="c9a8e-139">Las matrices VBA son OLE **SafeArrays**, definidas para C/C++ en los archivos de encabezado de Windows OLE/COM como **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-139">VBA arrays are OLE **SafeArrays**, defined for C/C++ in the Windows OLE/COM header files as **SAFEARRAY**.</span></span>
    
- <span data-ttu-id="c9a8e-140">El tipo de datos **Currency** de VBA se pasa como estructura de tipo **CY**, definido en el archivo wtypes.h del archivo de encabezado Windows, cuando pasa **ByVal**, y como un puntero para este cuando pasa **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-140">The VBA **Currency** data type is passed as a structure of type **CY**, defined in the Windows header file wtypes.h, when passed **ByVal**, and as a pointer to this when passed **ByRef**.</span></span>
    
<span data-ttu-id="c9a8e-141">En VBA, los elementos de los tipos de datos definidos por el usuario se empaquetan en l�mites de 4 bytes mientras que, en Visual Studio, de forma predeterminada, se empaquetan en l�mites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-141">In VBA, data elements in user-defined data types are packed to 4-byte boundaries, whereas in Visual Studio, by default, they are packed to 8-byte boundaries.</span></span> <span data-ttu-id="c9a8e-142">Por lo tanto, debe incluir la definición de la estructura de C/C++ en un bloque `#pragma pack(4) … #pragma pack()` para evitar que los elementos estén alineados de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-142">Therefore you must enclose the C/C++ structure definition in a  `#pragma pack(4) … #pragma pack()` block to avoid elements being misaligned.</span></span> 
  
<span data-ttu-id="c9a8e-143">El siguiente es un ejemplo de definiciones de tipo de usuario equivalente.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-143">The following is an example of equivalent user type definitions.</span></span>
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

<span data-ttu-id="c9a8e-p109">VBA admite una amplia gama de valores, en algunos casos, m�s de los que admite Excel. El doble de VBA es compatible con IEEE y admite n�meros por debajo de lo normal redondeados hacia abajo a cero en la hoja de cálculo. El tipo **Date** de VBA puede representar fechas anteriores al uno de enero de 0100 con fechas serializadas negativas. Excel solo permite fechas serializadas mayores o iguales a cero. El tipo **Currency** de VBA, un entero escalado de 64 bits, puede alcanzar una precisi�n no admitida por los dobles de 8 bytes y, por lo tanto, no coinciden en la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p109">VBA supports a greater range of values in some cases than Excel supports. The VBA double is IEEE compliant, supporting subnormal numbers that are currently rounded down to zero on the worksheet. The VBA **Date** type can represent dates as early as 1-Jan-0100 using negative serialized dates. Excel only allows serialized dates greater than or equal to zero. The VBA **Currency** type—a scaled 64-bit integer—can achieve accuracy not supported in 8-byte doubles, and so is not matched in the worksheet.</span></span> 
  
<span data-ttu-id="c9a8e-149">Excel solo pasa las variantes de los siguientes tipos a una función definida por el usuario de VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-149">Excel only passes Variants of the following types to a VBA user-defined function.</span></span>
  
|<span data-ttu-id="c9a8e-150">**Tipo de datos VBA**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-150">**VBA data type**</span></span>|<span data-ttu-id="c9a8e-151">**Marcas de bits de tipo Variant de C/C++**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-151">**C/C++ Variant type bit flags**</span></span>|<span data-ttu-id="c9a8e-152">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-152">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9a8e-153">Doble</span><span class="sxs-lookup"><span data-stu-id="c9a8e-153">Double</span></span>  <br/> |<span data-ttu-id="c9a8e-154">**VT_R8**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-154">**VT_R8**</span></span> <br/> ||
|<span data-ttu-id="c9a8e-155">Booleano</span><span class="sxs-lookup"><span data-stu-id="c9a8e-155">Boolean</span></span>  <br/> |<span data-ttu-id="c9a8e-156">**VT_BOOL**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-156">**VT_BOOL**</span></span> <br/> ||
|<span data-ttu-id="c9a8e-157">Fecha</span><span class="sxs-lookup"><span data-stu-id="c9a8e-157">Date</span></span>  <br/> |<span data-ttu-id="c9a8e-158">**VT_DATE**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-158">**VT_DATE**</span></span> <br/> ||
|<span data-ttu-id="c9a8e-159">String</span><span class="sxs-lookup"><span data-stu-id="c9a8e-159">String</span></span>  <br/> |<span data-ttu-id="c9a8e-160">**VT_BSTR**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-160">**VT_BSTR**</span></span> <br/> |<span data-ttu-id="c9a8e-161">Cadena de bytes Bstr OLE</span><span class="sxs-lookup"><span data-stu-id="c9a8e-161">OLE Bstr byte string</span></span>  <br/> |
|<span data-ttu-id="c9a8e-162">Range</span><span class="sxs-lookup"><span data-stu-id="c9a8e-162">Range</span></span>  <br/> |<span data-ttu-id="c9a8e-163">**VT_DISPATCH**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-163">**VT_DISPATCH**</span></span> <br/> |<span data-ttu-id="c9a8e-164">Referencias de celda y de rango</span><span class="sxs-lookup"><span data-stu-id="c9a8e-164">Range and cell references</span></span>  <br/> |
|<span data-ttu-id="c9a8e-165">Variante que contiene una matriz</span><span class="sxs-lookup"><span data-stu-id="c9a8e-165">Variant containing an array</span></span>  <br/> |<span data-ttu-id="c9a8e-166">**VT_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-166">**VT_ARRAY**</span></span> | <span data-ttu-id="c9a8e-167">**VT_VARIANT**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-167">**VT_VARIANT**</span></span> <br/> |<span data-ttu-id="c9a8e-168">Matrices literales</span><span class="sxs-lookup"><span data-stu-id="c9a8e-168">Literal arrays</span></span>  <br/> |
|<span data-ttu-id="c9a8e-169">Ccy</span><span class="sxs-lookup"><span data-stu-id="c9a8e-169">Ccy</span></span>  <br/> |<span data-ttu-id="c9a8e-170">**VT_CY**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-170">**VT_CY**</span></span> <br/> |<span data-ttu-id="c9a8e-171">Entero de 64 bits que se escala para permitir cuatro posiciones decimales de precisi�n.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-171">64-bit integer scaled to permit 4 decimal places of accuracy.</span></span>  <br/> |
|<span data-ttu-id="c9a8e-172">Variante que contiene un error</span><span class="sxs-lookup"><span data-stu-id="c9a8e-172">Variant containing an error</span></span>  <br/> |<span data-ttu-id="c9a8e-173">**VT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-173">**VT_ERROR**</span></span> <br/> ||
||<span data-ttu-id="c9a8e-174">**VT_EMPTY**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-174">**VT_EMPTY**</span></span> <br/> |<span data-ttu-id="c9a8e-175">Celdas vac�as o argumentos omitidos</span><span class="sxs-lookup"><span data-stu-id="c9a8e-175">Empty cells or omitted arguments</span></span>  <br/> |
   
<span data-ttu-id="c9a8e-p110">Puede comprobar el tipo de una variante pasada en VBA con **VarType**, excepto que la función devuelve el tipo de los valores del rango cuando se llama con referencias. Para determinar si una **Variant** es un objeto de referencia **Range**, puede usar la función **IsObject**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p110">You can check the type of a passed-in Variant in VBA using the **VarType**, except that the function returns the type of the range's values when called with references. To determine if a **Variant** is a **Range** reference object, you can use the **IsObject** function.</span></span> 
  
<span data-ttu-id="c9a8e-p111">Puede crear **Variants** que contenga matrices de variantes en VBA desde **Range** asignando la propiedad **Value** a **Variant**. Las celdas del rango de origen que tengan formato de moneda est�ndar para la configuraci�n regional en vigor en el momento, se convierten en elementos de matriz de tipo **Currency**. Las celdas con formato como fechas se convierten en elementos de la matriz de tipo **Date**. Las celdas que contienen cadenas se convierten en variantes **BSTR** de caracteres anchos. Las celdas que contienen errores se convierten en **Variants** de tipo **VT_ERROR**. Las celdas que contienen **Boolean** **True** o **False** se convierten en **Variants** de tipo **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p111">You can create **Variants** that contain arrays of variants in VBA from a **Range** by assigning its **Value** property to a **Variant**. Any cells in the source range that are formatted using the standard currency format for the regional settings in force at the time are converted to array elements of type **Currency**. Any cells formatted as dates are converted to array elements of type **Date**. Cells containing strings are converted to wide-character **BSTR** Variants. Cells containing errors are converted to **Variants** of type **VT_ERROR**. Cells containing **Boolean** **True** or **False** are converted to **Variants** of type **VT_BOOL**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c9a8e-p112">**Variant** almacena **True** como -1 y **False** como 0. Los n�meros sin formato como fechas o cantidades de moneda se convierten en variantes de tipo **VT_R8**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p112">The **Variant** stores **True** as -1 and **False** as 0. Numbers not formatted as dates or currency amounts are converted to Variants of type **VT_R8**.</span></span> 
  
### <a name="variant-and-string-arguments"></a><span data-ttu-id="c9a8e-186">Variante y argumentos de cadena</span><span class="sxs-lookup"><span data-stu-id="c9a8e-186">Variant and String Arguments</span></span>

<span data-ttu-id="c9a8e-p113">Excel funciona internamente con cadenas de caracteres anchos Unicode. Cuando se declara una función definida por el usuario VBA como que toma un argumento **String**, Excel convierte la cadena proporcionada en una cadena de bytes de forma espec�fica de la configuraci�n regional. Si quiere que la función se pase a una cadena Unicode, la función definida por el usuario VBA debe aceptar **Variant** en lugar de un argumento **String**. Luego, la función DLL la cadena de car�cter ancho BSTR **Variant** VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p113">Excel works internally with wide-character Unicode strings. When a VBA user-defined function is declared as taking a **String** argument, Excel converts the supplied string to a byte-string in a locale-specific way. If you want your function to be passed a Unicode string, your VBA user-defined function should accept a **Variant** instead of a **String** argument. Your DLL function can then accept that **Variant** BSTR wide-character string from VBA.</span></span> 
  
<span data-ttu-id="c9a8e-p114">Para devolver las cadenas Unicode a VBA desde un DLL, debe modificar un argumento de cadena **Variant** local. Para que funcione, debe declarar la función DLL que toma un puntero en **Variant** y en el códigode C/C++, y declarar el argumento en el códigoVBA como  `ByRef varg As Variant`. Debe liberar la memoria de cadena antigua y el nuevo valor de cadena creado con las funciones de cadena OLE Bstr solo en DLL.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p114">To return Unicode strings to VBA from a DLL, you should modify a **Variant** string argument in place. For this to work, you must declare the DLL function as taking a pointer to the **Variant** and in your C/C++ code, and declare the argument in the VBA code as  `ByRef varg As Variant`. The old string memory should be released, and the new string value created by using the OLE Bstr string functions only in the DLL.</span></span>
  
<span data-ttu-id="c9a8e-p115">Para devolver una cadena de bytes a VBA desde un DLL, debe modificar un argumento BSTR de cadena de bytes local. Para que funcione, debe declarar la función DLL que toma un puntero para un puntero en BSTR y en el códigode C/C++, y declarar el argumento en el códigoVBA como **ByRef varg As String**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p115">To return a byte string to VBA from a DLL, you should modify a byte-string BSTR argument in place. For this to work, you must declare the DLL function as taking a pointer to a pointer to the BSTR and in your C/C++ code, and declare the argument in the VBA code as ' **ByRef varg As String**'.</span></span>
  
<span data-ttu-id="c9a8e-p116">Solo debe gestionar las cadenas que se pasan de estas formas desde VBA con las funciones de cadena OLE BSTR para evitar problemas relacionados con la memoria. Por ejemplo, debe llamar a **SysFreeString** para liberar la memoria antes de sobrescribir la cadena pasada, y **SysAllocStringByteLen** o **SysAllocStringLen** para asignar espacio para una nueva cadena.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p116">You should only handle strings that are passed in these ways from VBA using the OLE BSTR string functions to avoid memory-related problems. For example, you must call **SysFreeString** to free the memory before overwriting the passed in string, and **SysAllocStringByteLen** or **SysAllocStringLen** to allocate space for a new string.</span></span> 
  
<span data-ttu-id="c9a8e-p117">Puede crear errores de hoja de cálculo de Excel como **Variants** en VBA con la función **CVerr** con argumentos, como se muestra en la siguiente tabla. Los errores de la hoja de cálculo tambi�n se pueden devolver a VBA desde un DLL con **Variants** de tipo **VT_ERROR**y con los siguientes valores en el campo **ulVal**.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p117">You can create Excel worksheet errors as **Variants** in VBA by using the **CVerr** function with arguments as shown in the following table. Worksheet errors can also be returned to VBA from a DLL using **Variants** of type **VT_ERROR**, and with the following values in the **ulVal** field.</span></span> 
  
|<span data-ttu-id="c9a8e-200">**Error**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-200">**Error**</span></span>|<span data-ttu-id="c9a8e-201">**Valor Variant ulVal**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-201">**Variant ulVal value**</span></span>|<span data-ttu-id="c9a8e-202">**Argumento CVerr**</span><span class="sxs-lookup"><span data-stu-id="c9a8e-202">**CVerr argument**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9a8e-203">#NULL!</span><span class="sxs-lookup"><span data-stu-id="c9a8e-203">#NULL!</span></span>  <br/> |<span data-ttu-id="c9a8e-204">2148141008</span><span class="sxs-lookup"><span data-stu-id="c9a8e-204">2148141008</span></span>  <br/> |<span data-ttu-id="c9a8e-205">2000</span><span class="sxs-lookup"><span data-stu-id="c9a8e-205">Windows 2000</span></span>  <br/> |
|<span data-ttu-id="c9a8e-206">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="c9a8e-206">#DIV/0!</span></span>  <br/> |<span data-ttu-id="c9a8e-207">2148141015</span><span class="sxs-lookup"><span data-stu-id="c9a8e-207">2148141015</span></span>  <br/> |<span data-ttu-id="c9a8e-208">2007</span><span class="sxs-lookup"><span data-stu-id="c9a8e-208">Word 2007</span></span>  <br/> |
|<span data-ttu-id="c9a8e-209">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="c9a8e-209">#VALUE!</span></span>  <br/> |<span data-ttu-id="c9a8e-210">2148141023</span><span class="sxs-lookup"><span data-stu-id="c9a8e-210">2148141023</span></span>  <br/> |<span data-ttu-id="c9a8e-211">2015</span><span class="sxs-lookup"><span data-stu-id="c9a8e-211">September 2015</span></span>  <br/> |
|<span data-ttu-id="c9a8e-212">#REF!</span><span class="sxs-lookup"><span data-stu-id="c9a8e-212">#REF!</span></span>  <br/> |<span data-ttu-id="c9a8e-213">2148141031</span><span class="sxs-lookup"><span data-stu-id="c9a8e-213">2148141031</span></span>  <br/> |<span data-ttu-id="c9a8e-214">2023</span><span class="sxs-lookup"><span data-stu-id="c9a8e-214">2023</span></span>  <br/> |
|<span data-ttu-id="c9a8e-215">#NAME?</span><span class="sxs-lookup"><span data-stu-id="c9a8e-215">#NAME?</span></span>  <br/> |<span data-ttu-id="c9a8e-216">2148141037</span><span class="sxs-lookup"><span data-stu-id="c9a8e-216">2148141037</span></span>  <br/> |<span data-ttu-id="c9a8e-217">2029</span><span class="sxs-lookup"><span data-stu-id="c9a8e-217">2029</span></span>  <br/> |
|<span data-ttu-id="c9a8e-218">#NUM!</span><span class="sxs-lookup"><span data-stu-id="c9a8e-218">#NUM!</span></span>  <br/> |<span data-ttu-id="c9a8e-219">2148141044</span><span class="sxs-lookup"><span data-stu-id="c9a8e-219">2148141044</span></span>  <br/> |<span data-ttu-id="c9a8e-220">2036</span><span class="sxs-lookup"><span data-stu-id="c9a8e-220">2036</span></span>  <br/> |
|<span data-ttu-id="c9a8e-221">#N/A</span><span class="sxs-lookup"><span data-stu-id="c9a8e-221">#N/A</span></span>  <br/> |<span data-ttu-id="c9a8e-222">2148141050</span><span class="sxs-lookup"><span data-stu-id="c9a8e-222">2148141050</span></span>  <br/> |<span data-ttu-id="c9a8e-223">2042</span><span class="sxs-lookup"><span data-stu-id="c9a8e-223">2042</span></span>  <br/> |
   
<span data-ttu-id="c9a8e-224">Tenga en cuenta que el valor **ulVal** variante dado equivale al valor de argumento **CVerr** más x800A0000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-224">Note that the Variant **ulVal** value given is equivalent to the **CVerr** argument value plus x800A0000 hexadecimal.</span></span> 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a><span data-ttu-id="c9a8e-225">Llamar a funciones DLL directamente desde la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="c9a8e-225">Calling DLL Functions Directly from the Worksheet</span></span>

<span data-ttu-id="c9a8e-p118">No puede acceder a funciones DLL de Win32 desde la hoja de cálculo sin, por ejemplo, usar VBA o XLM como interfaces, o sin dejar que Excel conozca la función, sus argumentos y el tipo devuelto por adelantado. Este proceso se denomina registro.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p118">You cannot access Win32 DLL functions from the worksheet without, for example, using VBA or XLM as interfaces, or without letting Excel know about the function, its arguments, and its return type in advance. The process of doing this is called registration.</span></span>
  
<span data-ttu-id="c9a8e-228">Las formas en que se puede acceder a las funciones de un DLL en la hoja de cálculo son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9a8e-228">The ways in which the functions of a DLL can be accessed in the worksheet are as follows:</span></span>
  
- <span data-ttu-id="c9a8e-229">Declarar la función de VBA como descrita anteriormente y acceder a ella a trav�s de una función definida por el usuario VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-229">Declare the function in VBA as described previously and access it via a VBA user-defined function.</span></span>
    
- <span data-ttu-id="c9a8e-230">Llamar a la función DLL con CALL en una hoja de macros XLM y acceder a ella a trav�s de una función definida por el usuario XLM.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-230">Call the DLL function using CALL on an XLM macro sheet, and access it via an XLM user-defined function.</span></span>
    
- <span data-ttu-id="c9a8e-231">Usar un comando XLM o VBA para llamar a la función **REGISTER** de XML, que proporciona la información que Excel necesita para reconocer la función cuando se introduce en una celda de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-231">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information that Excel needs to recognize the function when it is entered into a worksheet cell.</span></span> 
    
- <span data-ttu-id="c9a8e-232">Convertir el DLL en un XLL y registrar la función con la función **xlfRegister** de la API de C cuando se activa XLL.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-232">Turn the DLL into an XLL and register the function using the C API **xlfRegister** function when the XLL is activated.</span></span> 
    
<span data-ttu-id="c9a8e-p119">El cuarto enfoque es independiente: el códigoque registra las funciones y el códigode función se incluyen en el mismo proyecto de código. Realizar cambios en el complemento no implica realizar cambios a una hoja de XLM o en un m�dulo de códigoVBA. Para hacerlo de manera administrada manteni�ndose dentro de las capacidades de la API de C, debe convertir el DLL en un XLL y cargar el complemento resultante con Administrador de complementos. Esto permite que Excel llame a una función que expone el DLL cuando se carga o activa el complemento, desde el que puede registrar todas las funciones que contiene el XLL y realizar cualquier otra inicializaci�n del DLL.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p119">The fourth approach is self-contained: the code that registers the functions and the function code are both contained in the same code project. Making changes to the add-in does not involve making changes to an XLM sheet or to a VBA code module. To do this in a well-managed way while still staying within the capabilities of the C API, you must turn your DLL into an XLL and load the resulting add-in by using the Add-in Manager. This enables Excel to call a function that your DLL exposes when the add-in is loaded or activated, from which you can register all of the functions your XLL contains, and carry out any other DLL initialization.</span></span>
  
## <a name="calling-dll-commands-directly-from-excel"></a><span data-ttu-id="c9a8e-237">Llamar a los comandos DLL directamente desde Excel</span><span class="sxs-lookup"><span data-stu-id="c9a8e-237">Calling DLL Commands Directly from Excel</span></span>

<span data-ttu-id="c9a8e-238">No se puede acceder directamente a los comandos del DLL de Win32 desde los men�s y los cuadros de di�logo de Excel sin que haya una interfaz, como VBA, o sin los comandos que se registran con antelaci�n.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-238">Win32 DLL commands are not accessible directly from Excel dialog boxes and menus without there being an interface, such as VBA, or without the commands being registered in advance.</span></span>
  
<span data-ttu-id="c9a8e-239">Las formas en las que acceder a los comandos de un DLL son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9a8e-239">The ways in which you can access the commands of a DLL are as follows:</span></span>
  
- <span data-ttu-id="c9a8e-240">Declarar el comando de VBA, como se describi� anteriormente, y acceder a �l a trav�s de una macro de VBA.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-240">Declare the command in VBA as described previously and access it via a VBA macro.</span></span>
    
- <span data-ttu-id="c9a8e-241">Llamar al comando DLL con **CALL** en una hoja de macros XLM y acceder a �l a trav�s de una macro XLM.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-241">Call the DLL command using **CALL** on an XLM macro sheet, and access it via an XLM macro.</span></span> 
    
- <span data-ttu-id="c9a8e-242">Usar un comando XLM o VBA para llamar a la función **REGISTER** de XML, que proporciona la información que Excel necesita para reconocer el comando cuando se introduce en un cuadro de di�logo que se espera el nombre de un comando de macros.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-242">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information Excel needs to recognize the command when it is entered into a dialog box that expects the name of a macro command.</span></span> 
    
- <span data-ttu-id="c9a8e-243">Convertir el DLL en un XLL y registrar el comando mediante la función **xlfRegister** de la API de C.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-243">Turn the DLL into an XLL and register the command using the C API **xlfRegister** function.</span></span> 
    
<span data-ttu-id="c9a8e-p120">Como se ha explicado anteriormente, en el contexto de las funciones DLL, el cuarto enfoque es el m�s independiente ya que mantiene el códigode registro cerca del códigode comando. Para ello, debe convertir el DLL en un XLL y cargar el complemento resultante con el Administrador de complementos. Registrar los comandos de esta manera tambi�n le permite adjuntar el comando a un elemento de la interfaz de usuario, como un men� personalizado, o configurar una captura de eventos que llame al comando en una pulsaci�n de tecla determinada u otro evento.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p120">As discussed earlier in the context of DLL functions, the fourth approach is the most self-contained, keeping the registration code close to the command code. To do this, you must turn your DLL into an XLL and load the resulting add-in using the Add-in Manager. Registering commands in this way also lets you attach the command to an element of the user interface, such as a custom menu, or to set up an event trap that calls the command on a given keystroke or other event.</span></span>
  
<span data-ttu-id="c9a8e-247">Excel asume que todos los comandos XLL registrados con Excel tienen el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-247">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> <span data-ttu-id="c9a8e-p121">Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p121">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span> 
  
## <a name="dll-memory-and-multiple-dll-instances"></a><span data-ttu-id="c9a8e-250">Memoria de DLL e instancias de varios DLL</span><span class="sxs-lookup"><span data-stu-id="c9a8e-250">DLL Memory and Multiple DLL Instances</span></span>

<span data-ttu-id="c9a8e-p122">Cuando una aplicación carga un DLL, el códigoejecutable del DLL se carga en el mont�n global para que se pueda ejecutar, y se asigna espacio en el mont�n global para las estructuras de datos. Windows usa la asignaci�n de memoria para que estas �reas de memoria aparezcan como si estuvieran en el proceso de la aplicación, para que esta pueda acceder a ella.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p122">When an application loads a DLL, the DLL's executable code is loaded into the global heap so that it can be run, and space is allocated on the global heap for its data structures. Windows uses memory mapping to make these areas of memory appear as if they are in the application's process so that the application can access them.</span></span>
  
<span data-ttu-id="c9a8e-p123">Si una segunda aplicación carga el DLL, Windows no crea otra copia del códigoejecutable de DLL, ya que la memoria es de solo lectura. Windows asigna la memoria de códigoejecutable de DLL a los procesos de ambas aplicaciones. Sin embargo, asigna un segundo espacio para una copia privada de las estructuras de datos del DLL y asigna esta copia solo al segundo proceso. Esto garantiza que ninguna aplicación interfiere con los datos del DLL de la otra.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p123">If a second application then loads the DLL, Windows does not make another copy of the DLL executable code, as that memory is read-only. Windows maps the DLL executable code memory to the processes of both applications. It does, however, allocate a second space for a private copy of the DLL's data structures and maps this copy to the second process only. This ensures that neither application can interfere with the DLL data of the other.</span></span>
  
<span data-ttu-id="c9a8e-p124">Esto significa que los desarrolladores de DLL no tienen que preocuparse de las variables globales y est�ticas ni de las estructuras de datos a las que acceden varias aplicaciones, o m�s de una instancia de la misma aplicación. Cada instancia de cada aplicación obtiene su propia copia de los datos del DLL.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p124">This means that DLL developers do not have to be concerned about static and global variables and data structures being accessed by more than one application, or more than one instance of the same application. Every instance of every application gets its own copy of the DLL's data.</span></span>
  
<span data-ttu-id="c9a8e-p125">Los desarrolladores de DLL no tienen que preocuparse por la misma instancia de una aplicación que llama al DLL varias veces desde distintos subprocesos, ya que esto puede provocar la contenci�n de los datos de esa instancia. Para obtener m�s información, consulte [administración de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="c9a8e-p125">DLL developers do need to be concerned about the same instance of an application calling their DLL many times from different threads, because this can result in contention for that instance's data. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9a8e-261">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9a8e-261">See also</span></span>

- [<span data-ttu-id="c9a8e-262">Desarrollar DLL</span><span class="sxs-lookup"><span data-stu-id="c9a8e-262">Developing DLLs</span></span>](developing-dlls.md) 
- [<span data-ttu-id="c9a8e-263">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="c9a8e-263">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)

