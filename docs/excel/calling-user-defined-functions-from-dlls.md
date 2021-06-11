---
title: Llamar a funciones definidas por el usuario desde DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], llamadas desde dlls,funciones definidas por el usuario [Excel 2007], llamadas desde DLL,DLL [Excel 2007], llamadas a UDF
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417948"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="8b1d6-104">Llamar a funciones definidas por el usuario desde DLL</span><span class="sxs-lookup"><span data-stu-id="8b1d6-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="8b1d6-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b1d6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8b1d6-106">Llamar a funciones definidas por el usuario (UDF) desde una hoja de cálculo es tan simple como llamar a funciones integradas: se escribe la función a través de una fórmula de celda.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="8b1d6-107">Sin embargo, desde la API de C, no hay códigos de función predefinidos para usar con las llamadas atrás.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="8b1d6-108">Para que pueda llamar a UDF, la API de C exporta una función de solo XLL, la [función xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="8b1d6-109">El primer argumento de la función es el nombre de la función como una cadena y los argumentos posteriores son los que normalmente esperaría la UDF.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="8b1d6-110">Puede obtener una lista de las funciones y comandos del complemento XLL registrados actualmente mediante la función **xlfGetWorkspace** con el argumento 44.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="8b1d6-111">Esto devuelve una matriz de tres columnas donde las columnas representan lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="8b1d6-112">La ruta de acceso completa y el nombre del XLL</span><span class="sxs-lookup"><span data-stu-id="8b1d6-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="8b1d6-113">Nombre de udf o comando exportado desde XLL</span><span class="sxs-lookup"><span data-stu-id="8b1d6-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="8b1d6-114">La cadena de código return y argument</span><span class="sxs-lookup"><span data-stu-id="8b1d6-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="8b1d6-115">Es posible que el nombre exportado desde XLL no sea el mismo que el nombre registrado por el que Excel conoce la UDF o el comando.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="8b1d6-116">A partir de Excel 2007, las funciones de Analysis Toolpak (ATP) están totalmente integradas y la API de C tiene sus propias enumeraciones para funciones como PRICE, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="8b1d6-117">En versiones anteriores, tenías que usar **xlUDF para** llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="8b1d6-118">Si el complemento necesita trabajar con Excel 2003 y Excel 2007 o versiones posteriores, y usa estas funciones, debe detectar la versión actual y llamar a la función de la manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="8b1d6-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b1d6-119">Examples</span></span>

<span data-ttu-id="8b1d6-120">En el ejemplo siguiente se muestra la función **xlUDF** que se usa para llamar a la función ATP **PRICE** cuando la versión en ejecución de Excel es 2003 o anterior.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="8b1d6-121">Para obtener información sobre la configuración de una variable de versión global, como **gExcelVersion12plus** en este ejemplo, vea [Compatibilidad con versiones anteriores](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="8b1d6-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8b1d6-122">En este ejemplo se usan las funciones Framework **TempNum**, **TempStrConst** para configurar los argumentos y Excel para llamar a la API de C.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="8b1d6-123">Cuando se llama a una función XLL que devuelve un valor modificando un argumento en su lugar, la función **xlUDF** aún devuelve el valor a través de la dirección del resultado **XLOPER/XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="8b1d6-124">En otras palabras, el resultado se devuelve como si a través de una instrucción return normal.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="8b1d6-125">El **XLOPER/XLOPER12** que corresponde al argumento que se usa para el valor devuelto no estámodificado.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="8b1d6-126">Por ejemplo, tenga en cuenta las dos UDF siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="8b1d6-127">Cuando **UDF \_ 2** llama **a UDF \_ 1**, el valor de **pxArg** no cambia después de la llamada a **Excel12** y el valor devuelto por **UDF_1** se encuentra en **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="8b1d6-128">Cuando realiza un gran número de llamadas a una UDF de esta manera, puede evaluar el nombre de la función primero mediante la función [xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="8b1d6-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="8b1d6-129">El número resultante, que es el mismo que el identificador de registro devuelto por la función **xlfRegister,** se puede pasar en lugar del nombre de la función como primer argumento a la función **xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="8b1d6-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="8b1d6-130">Esto permite Excel buscar y llamar a la función más rápidamente que si tiene que buscar el nombre de la función cada vez.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b1d6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b1d6-131">See also</span></span>

- [<span data-ttu-id="8b1d6-132">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="8b1d6-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="8b1d6-133">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="8b1d6-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="8b1d6-134">Introducción al SDK de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="8b1d6-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

