---
title: Llamada a funciones definidas por el usuario desde las DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDF [excel 2007], llamar desde DLL, funciones definidas por el usuario [Excel 2007], llamar desde DLL, archivos DLL [Excel 2007], al llamar a las UDF
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815530"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="9ba29-104">Llamada a funciones definidas por el usuario desde las DLL</span><span class="sxs-lookup"><span data-stu-id="9ba29-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="9ba29-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ba29-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9ba29-106">Llamar a funciones definidas por el usuario (UDF) desde una hoja de cálculo es tan sencillo como llamar a funciones integradas: escriba la función a través de una fórmula de celda.</span><span class="sxs-lookup"><span data-stu-id="9ba29-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="9ba29-107">Sin embargo, de la API de C, no hay ningún código de función predefinidos para usar con las devoluciones de llamadas.</span><span class="sxs-lookup"><span data-stu-id="9ba29-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="9ba29-108">Para que se pueda llamar a las UDF, la API C exporta una función sólo XLL, la función [xlUDF](xludf.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba29-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="9ba29-109">Primer argumento de la función es el nombre de la función como una cadena, y los argumentos subsiguientes son los que normalmente se esperaría la UDF.</span><span class="sxs-lookup"><span data-stu-id="9ba29-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="9ba29-110">Puede obtener una lista de los comandos y actualmente registrado XLL en Agregar funciones mediante el uso de la función **xlfGetWorkspace** con el argumento 44.</span><span class="sxs-lookup"><span data-stu-id="9ba29-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="9ba29-111">Esto devuelve una matriz de tres columnas donde las columnas representan lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ba29-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="9ba29-112">La ruta de acceso completa y el nombre del XLL</span><span class="sxs-lookup"><span data-stu-id="9ba29-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="9ba29-113">El nombre del comando como exportado desde el XLL o UDF</span><span class="sxs-lookup"><span data-stu-id="9ba29-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="9ba29-114">La cadena de código de retorno y el argumento</span><span class="sxs-lookup"><span data-stu-id="9ba29-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="9ba29-115">El nombre como exportado desde el XLL no puede ser el mismo que el nombre registrado por el que Excel sepa el UDF o el comando.</span><span class="sxs-lookup"><span data-stu-id="9ba29-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="9ba29-116">Iniciar en Excel 2007, las funciones de herramientas para análisis (ATP) están completamente integradas y la API C tiene sus propio enumeraciones para funciones como precio, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="9ba29-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="9ba29-117">En versiones anteriores, había que usar **xlUDF** para llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="9ba29-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="9ba29-118">Si el complemento que se necesita para que funcione con Excel 2003 y Excel 2007 o versiones posteriores, y se utiliza estas funciones, debe detectar la versión actual y llame a la función de la manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="9ba29-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="9ba29-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9ba29-119">Examples</span></span>

<span data-ttu-id="9ba29-120">En el ejemplo siguiente se muestra la función **xlUDF** que se utiliza para llamar a la función ATP **precio** cuando la versión en ejecución de Excel 2003 o anterior.</span><span class="sxs-lookup"><span data-stu-id="9ba29-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="9ba29-121">Para obtener información acerca de la configuración de una variable global versión, como **gExcelVersion12plus** en este ejemplo, consulte [Compatibilidad con versiones anteriores](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="9ba29-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ba29-122">En este ejemplo se utilizan las funciones de marco de trabajo **TempNum**, **TempStrConst** para configurar los argumentos y Excel para llamar a la API de C.</span><span class="sxs-lookup"><span data-stu-id="9ba29-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

<span data-ttu-id="9ba29-123">Donde está llamando a una función XLL que devuelve un valor mediante la modificación de un argumento en su lugar, la función **xlUDF** todavía devuelve el valor a través de la dirección del resultado **XLOPER y XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9ba29-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="9ba29-124">En otras palabras, se devuelve el resultado como si a través de una instrucción return normal.</span><span class="sxs-lookup"><span data-stu-id="9ba29-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="9ba29-125">**XLOPER y XLOPER12** que corresponde al argumento que se usa para el valor devuelto es sin modificar.</span><span class="sxs-lookup"><span data-stu-id="9ba29-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="9ba29-126">Por ejemplo, considere la posibilidad de las UDF de dos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ba29-126">For example, consider the following two UDFs.</span></span> 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

<span data-ttu-id="9ba29-127">Cuando **UDF\_2** llamadas **UDF\_1**, el valor de **pxArg** no ha cambiado después de llamar a **Excel12**, y el valor devuelto por **UDF_1** se encuentra en **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="9ba29-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="9ba29-128">Cuando se va a realizar un gran número de llamadas a una UDF de esta manera, puede evaluar el nombre de la función mediante la [función xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="9ba29-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="9ba29-129">El número resultante, que es el mismo que el identificador de registro que es devuelto por la función **xlfRegister** , se puede pasar en lugar del nombre de función como primer argumento a la función **xlUDF** .</span><span class="sxs-lookup"><span data-stu-id="9ba29-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="9ba29-130">Esto permite que Excel buscar y llamar a la función más rápidamente que si tiene que buscar el nombre de la función de cada vez.</span><span class="sxs-lookup"><span data-stu-id="9ba29-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ba29-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ba29-131">See also</span></span>

- [<span data-ttu-id="9ba29-132">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="9ba29-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="9ba29-133">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="9ba29-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="9ba29-134">Introducción al SDK de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="9ba29-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

