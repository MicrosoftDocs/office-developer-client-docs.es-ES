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
# <a name="calling-user-defined-functions-from-dlls"></a>Llamada a funciones definidas por el usuario desde las DLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamar a funciones definidas por el usuario (UDF) desde una hoja de cálculo es tan sencillo como llamar a funciones integradas: escriba la función a través de una fórmula de celda. Sin embargo, de la API de C, no hay ningún código de función predefinidos para usar con las devoluciones de llamadas. Para que se pueda llamar a las UDF, la API C exporta una función sólo XLL, la función [xlUDF](xludf.md) . Primer argumento de la función es el nombre de la función como una cadena, y los argumentos subsiguientes son los que normalmente se esperaría la UDF. 
  
Puede obtener una lista de los comandos y actualmente registrado XLL en Agregar funciones mediante el uso de la función **xlfGetWorkspace** con el argumento 44. Esto devuelve una matriz de tres columnas donde las columnas representan lo siguiente: 
  
- La ruta de acceso completa y el nombre del XLL
    
- El nombre del comando como exportado desde el XLL o UDF
    
- La cadena de código de retorno y el argumento
    
> [!NOTE]
> El nombre como exportado desde el XLL no puede ser el mismo que el nombre registrado por el que Excel sepa el UDF o el comando. 
  
Iniciar en Excel 2007, las funciones de herramientas para análisis (ATP) están completamente integradas y la API C tiene sus propio enumeraciones para funciones como precio, **xlfPrice**. En versiones anteriores, había que usar **xlUDF** para llamar a estas funciones. Si el complemento que se necesita para que funcione con Excel 2003 y Excel 2007 o versiones posteriores, y se utiliza estas funciones, debe detectar la versión actual y llame a la función de la manera adecuada. 
  
## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la función **xlUDF** que se utiliza para llamar a la función ATP **precio** cuando la versión en ejecución de Excel 2003 o anterior. Para obtener información acerca de la configuración de una variable global versión, como **gExcelVersion12plus** en este ejemplo, consulte [Compatibilidad con versiones anteriores](backward-compatibility.md).
  
> [!NOTE]
> En este ejemplo se utilizan las funciones de marco de trabajo **TempNum**, **TempStrConst** para configurar los argumentos y Excel para llamar a la API de C. 
  
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

Donde está llamando a una función XLL que devuelve un valor mediante la modificación de un argumento en su lugar, la función **xlUDF** todavía devuelve el valor a través de la dirección del resultado **XLOPER y XLOPER12**. En otras palabras, se devuelve el resultado como si a través de una instrucción return normal. **XLOPER y XLOPER12** que corresponde al argumento que se usa para el valor devuelto es sin modificar. Por ejemplo, considere la posibilidad de las UDF de dos siguientes. 
  
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

Cuando **UDF\_2** llamadas **UDF\_1**, el valor de **pxArg** no ha cambiado después de llamar a **Excel12**, y el valor devuelto por **UDF_1** se encuentra en **xRetVal**.
  
Cuando se va a realizar un gran número de llamadas a una UDF de esta manera, puede evaluar el nombre de la función mediante la [función xlfEvaluate](xlfevaluate.md). El número resultante, que es el mismo que el identificador de registro que es devuelto por la función **xlfRegister** , se puede pasar en lugar del nombre de función como primer argumento a la función **xlUDF** . Esto permite que Excel buscar y llamar a la función más rápidamente que si tiene que buscar el nombre de la función de cada vez. 
  
## <a name="see-also"></a>Vea también

- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

