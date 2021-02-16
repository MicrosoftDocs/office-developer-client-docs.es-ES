---
title: Llamar a funciones definidas por el usuario desde DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], calling from dlls,user-defined functions [Excel 2007], calling from DLLs,DLLs [Excel 2007], calling UDFs
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
# <a name="calling-user-defined-functions-from-dlls"></a>Llamar a funciones definidas por el usuario desde DLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamar a funciones definidas por el usuario (UDF) desde una hoja de cálculo es tan sencillo como llamar a funciones integradas: la función se especifica a través de una fórmula de celda. Sin embargo, desde la API de C, no hay códigos de función predefinidos para usar con las llamadas. Para permitirle llamar a udf, la API de C exporta una función solo XLL, la [función xlUDF.](xludf.md) El primer argumento de la función es el nombre de la función como una cadena y los argumentos posteriores son los que normalmente esperaría la UDF. 
  
Puede obtener una lista de las funciones y comandos del complemento XLL registrados actualmente mediante la función **xlfGetWorkspace** con el argumento 44. Devuelve una matriz de tres columnas en la que las columnas representan lo siguiente: 
  
- La ruta de acceso completa y el nombre del XLL
    
- El nombre de la UDF o el comando exportado desde el XLL
    
- La cadena de código de devolución y argumento
    
> [!NOTE]
> Es posible que el nombre exportado desde el XLL no sea el mismo que el nombre registrado por el que Excel conoce la UDF o el comando. 
  
A partir de Excel 2007, las funciones de Analysis Toolpak (ATP) están completamente integradas y la API de C tiene sus propias enumeraciones para funciones como PRICE, **xlfPrice**. En versiones anteriores, tenía que usar **xlUDF para** llamar a estas funciones. Si el complemento necesita trabajar con Excel 2003 y Excel 2007 o versiones posteriores, y usa estas funciones, debe detectar la versión actual y llamar a la función de la forma adecuada. 
  
## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra la función **xlUDF** que se usa para llamar a la función ATP **PRICE** cuando la versión en ejecución de Excel es 2003 o anterior. Para obtener información sobre la configuración de una variable de versión global, como **gExcelVersion12plus** en este ejemplo, vea [Compatibilidad con versiones anteriores.](backward-compatibility.md)
  
> [!NOTE]
> En este ejemplo se usan las funciones de marco **TempNum**, **TempStrConst** para configurar los argumentos y Excel para llamar a la API de C. 
  
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

Donde se llama a una función XLL que devuelve un valor modificando un argumento en su lugar, la función **xlUDF** todavía devuelve el valor a través de la dirección del resultado **XLOPER/XLOPER12**. En otras palabras, el resultado se devuelve como si se hubiera a través de una instrucción return normal. El **XLOPER/XLOPER12** que corresponde al argumento que se usa para el valor devuelto no se hamodificado. Por ejemplo, tenga en cuenta las dos UDF siguientes. 
  
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

Cuando **UDF \_ 2** llama **a UDF \_ 1**, el valor de **pxArg** no cambia después de la llamada a **Excel12** y el valor devuelto por **UDF_1** se encuentra en **xRetVal**.
  
Cuando se realiza un gran número de llamadas a una UDF de esta manera, puede evaluar el nombre de la función primero mediante la función [xlfEvaluate](xlfevaluate.md). El número resultante, que es el mismo que el identificador de registro devuelto por la función **xlfRegister,** se puede pasar en lugar del nombre de la función como primer argumento a la función **xlUDF.** Esto permite a Excel buscar y llamar a la función más rápidamente que si tiene que buscar el nombre de la función cada vez. 
  
## <a name="see-also"></a>Consulte también

- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

