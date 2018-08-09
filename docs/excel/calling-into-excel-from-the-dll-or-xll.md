---
title: Llamar a Excel desde el DLL o XLL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- comandos, archivos DLL [Excel 2007], llamada en Excel, pasar argumentos a funciones de la API de C [Excel 2007], [Excel 2007], los comandos de excel de cuadros de diálogo [excel 2007], invocación de invocar con cuadros de diálogo, comandos [Excel 2007], accesibles desde el archivo DLL o XLL, Excel4 funcionan [ Función de Excel12 de Excel 2007], [Excel 2007], XLCallVer funcionar el argumento de operRes [Excel 2007], [Excel 2007], funciones [Excel 2007], accesibles desde el archivo DLL o XLL, Excel12v funcionan [Excel 2007], sólo DLL funciona API de C [Excel 2007], [Excel 2007], pasar recuento de argumentos, argumento [Excel 2007], comandos [Excel 2007], al llamar a las versiones internacionales, sólo DLL comandos [Excel 2007], las versiones internacionales [Excel 2007], llamada a funciones y comandos, XLL [Excel 2007], llamada a Excel, Excel 4v función [ Excel 2007], xlfn argumento [Excel 2007], [Excel 2007], funciones de llamada en las versiones internacionales
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815574"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Llamar a Excel desde el DLL o XLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel permite que el archivo DLL tener acceso a comandos integrados de Excel, funciones de hoja de cálculo y las funciones de hoja de macro. Se encuentran disponibles tanto de los comandos del archivo DLL y las funciones llamadas desde Visual Basic para aplicaciones (VBA) y de funciones llamadas directamente por Excel y comandos XLL registrados.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4, Excel4v, Excel12 y funciones Excel12v

Excel permite que el archivo DLL tener acceso a los comandos y las funciones a través de las funciones de devolución de llamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)y [Excel12v](excel4v-excel12v.md).
  
Las funciones de **Excel4** y **Excel4v** se introdujeron en Excel versión 4. Trabajar con la estructura de datos **XLOPER** . Excel 2007 introdujo dos nuevas funciones de devolución de llamada, **Excel12** y **Excel12v**, que funcionan con la estructura de datos **XLOPER12** . Las funciones de **Excel4** y **Excel4v** se exportan en la biblioteca de Xlcall32.lib, que debe estar incluido en el proyecto de DLL o XLL. **Excel12** y **Excel12v** se incluyen en el archivo de origen C++ SDK Xlcall.cpp, que se debe incluir en el proyecto si desea tener acceso a la funcionalidad de Excel mediante el uso de estructuras **XLOPER12** . 
  
El código siguiente muestra los prototipos de función para estas cuatro funciones. Los tres primeros argumentos son los mismos, excepto en que el segundo argumento es un puntero a un **XLOPER** en el primer par y un puntero a un **XLOPER12** en el segundo par. La convención de llamada es **_cdecl** en **Excel4** y **Excel12** para permitir que las listas de argumentos de variable. Los puntos suspensivos representa punteros a los valores **XLOPER** de **Excel4** y **XLOPER12** valores para **Excel12**. El número de punteros es igual al valor del parámetro _count_ . 
  
**Todas las versiones de Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**A partir de Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Para que el archivo DLL poder llamar a **Excel4**, **Excel4v**, **Excel12**o **Excel12v**, Excel debe pasar el control a la DLL. Esto significa que se pueden llamar a estas devoluciones de llamada de la API C sólo en los siguientes escenarios:
  
- Desde un comando de XLL de Excel ha llamado directamente o a través de VBA.
    
- Desde dentro de una función de hoja de hoja de cálculo o una macro XLL que Excel ha llamado directamente o a través de VBA.
    
No se puede llamar a la API de C de Excel en los siguientes escenarios:
  
- Desde un evento de sistema operativo (por ejemplo, de la función [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) ). 
    
- Desde un subproceso de fondo que crea el archivo DLL.
    
### <a name="return-values"></a>Valores devueltos

Cuatro de estas funciones devuelve un valor entero que se informa de si la función o el comando recibió correctamente el autor de la llamada. Los valores devueltos pueden ser cualquiera de las siguientes opciones:
  
|**Valor devuelto**|**Definido en Xlcall.h como**|**Descripción**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La función o el comando que se ejecutó correctamente. Esto no significa que la ejecución ha producido error gratuita. Por ejemplo, **Excel4** podría devolver **xlretSuccess** cuando se llama a la función **Buscar**, aunque evalúan hasta **#VALUE!** debido a que no se pudo encontrar el texto de búsqueda. Inspeccione el tipo y el valor de devuelto **XLOPER y XLOPER12** donde esto es una posibilidad.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Una macro de comando se detuvo por el usuario hace clic en el botón **Cancelar** o al presionar la tecla ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |El código de comando o función proporcionado no es válido. Este error puede producirse cuando la función de llamada no tiene permiso para llamar a la función o el comando. Por ejemplo, una función de hoja de cálculo no puede llamar a una función de información de hoja de macro o un comando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |El número de argumentos proporcionado en la llamada no es correcto.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Uno o varios de los valores del argumento **XLOPER** o **XLOPER12** correctamente no están formado o se rellena.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel detectó un riesgo de que la operación es posible que su pila de desbordamiento y, por lo tanto, no llame a la función.  <br/> |
|32  <br/> |**xlretFailed** <br/> |El comando o la función no se pudo por un motivo no descrito por uno de los otros valores devueltos. Una operación que sería necesario demasiada memoria, por ejemplo, se producirá un error con este error. Esto puede suceder durante un intento de convertir una referencia a una matriz **xltypeMulti** muy grande mediante el uso de la función [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) .  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Se ha intentado la operación recuperar el valor de una celda no calculada. Para conservar la integridad de los cálculos en Excel, funciones de hoja de cálculo no se permiten hacer esto. Sin embargo, las funciones y comandos XLL registran como funciones de hoja de macros se pueden tener acceso a los valores de celda no calculada.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Comenzando en Excel 2007) Una función de hoja de cálculo XLL registrada como seguros para subprocesos ha intentado llamar a una función de la API de C que no es segura para subprocesos. Por ejemplo, una función de subprocesos no puede llamar a la función XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Comenzando en Excel 2010) El identificador de función asincrónica no es válido.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Comenzando en Excel 2010) La llamada no se admite en clústeres.  <br/> |
   
Si la función devuelve uno de los valores de error en la tabla (es decir, no devuelve **xlretSuccess**), el valor devuelto **XLOPER** o **XLOPER12** también se establecerá en **#VALUE!**. En determinadas circunstancias, para esto puede resultar una prueba suficiente de éxito, pero debe tener en cuenta que una llamada puede devolver ambos **xlretSuccess** de comprobación y **#VALUE!**.
  
Si una llamada a los resultados de la API C en **xlretUncalced** o **xlretAbort**, el código de la DLL o XLL debe devolver el control a Excel antes de realizar otras llamadas API C (que no sean llamadas a la función [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) para liberar memoria asignada en Excel recursos en los valores **XLOPER** y **XLOPER12** ). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Comando o un argumento de función (enumeración): xlfn

El argumento _xlfn_ es el primer argumento a la devolución de llamada funciona y es un entero con signo de 32 bits. Su valor debe ser una de las enumeraciones de función o un comando definidas en el archivo de encabezado SDK Xlcall.h, tal como se muestra en el siguiente ejemplo. 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

Hoja de hoja de cálculo y de macros todas las funciones están en el intervalo entre 0 (**xlfCount**) a través de 0x0fff hexadecimal, aunque había asignado el mayor número de Excel 2013 es 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).
  
Todas las funciones de comando se encuentran en el intervalo de 0 x 8000 hexadecimal (**xlcBeep**) a través de 0x8fff hexadecimal, aunque el número más alto asignado en Excel 2013 es 0x8328 hexadecimal (**xlcHideallInkannots**). Se definen en el archivo de encabezado como `(n | xlCommand)` donde `n` es un número decimal mayor o igual a 0 y **xlCommand** se define como 0 x 8000 hexadecimal. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Invocar los comandos de Excel que utilizar cuadros de diálogo

Algunos de los códigos de comando corresponden a acciones en Excel que utilizar cuadros de diálogo. Por ejemplo, **xlcFileDelete** toma un único argumento: un nombre de archivo o máscara. Esto se puede invocar con el cuadro de diálogo para que el usuario tiene la oportunidad de cancelar o modificar la operación de eliminación. Se puede también llamar sin el cuadro de diálogo, en cuyo caso se eliminan el archivo o archivos sin interacción más, suponiendo que existan y el autor de la llamada tiene permiso. Para llamar a esos comandos en su formulario de cuadro de diálogo, se debe combinar la enumeración de comando mediante el uso de la operación OR bit a bit con 0 x 1000 (**xlPrompt**).
  
En el ejemplo de código siguiente se elimina los archivos en el directorio actual que coinciden con la máscara my_data\*.bak, mostrar un cuadro de diálogo sólo si el argumento es true.
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>Llamada a funciones y comandos de las versiones internacionales

Puede configurar Excel para mostrar las funciones y nombres de los comandos XLM en una gran variedad de idiomas. Algunos comandos de la API de C y funciones funcionan en cadenas que se interpretan como nombres de función o un comando. Por ejemplo, **xlcFormula** toma un argumento de cadena que está pensado para colocarse en una celda especificada. Para el complemento para que funcione con todas las opciones de idioma, puede proporcionar los nombres de cadena en inglés y establecer el bit 0 x 2000 (**xlIntl**) en la enumeración de función o un comando.
  
En el ejemplo de código siguiente se coloca el equivalente de `=SUM(X1:X100)` en la celda A2 de la hoja activa. Tenga en cuenta que usa la función de Framework, **TempActiveRef**, para crear una referencia externa temporal **XLOPER**. La fórmula aparecerá en A2 en el idioma correcto de determinada configuración regional (por ejemplo, `=SOMME(X1:X100)` si el idioma es francés). 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> Debido a que el resultado de la llamada a **Excel12** no es necesario, se podría pasar cero (NULL) como el segundo argumento en lugar de la dirección de **xResult**. Esto se explica más en la siguiente sección. 
  
### <a name="dll-only-functions-and-commands"></a>Comandos y funciones sólo DLL

Excel admite un número reducido de funciones que sólo son accesibles desde una DLL o XLL. Se definen en el archivo de encabezado como `(n | xlSpecial)` donde `n` es un número decimal mayor o igual a 0 y `xlSpecial` se define como 0 x 4000 hexadecimal. Estas funciones están enumeradas en la siguiente tabla y documentadas en la [Referencia de función de la API](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Libera los recursos de memoria asignada en Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Devuelve el espacio libre en la pila de Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Convierte entre tipos **XLOPER** y **XLOPER12**  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Proporciona un método rápido de establecer valores de celda.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Obtiene un nombre de hoja de cálculo de su identificador interno.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Obtiene un identificador interno de la hoja de cálculo de su nombre.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Comprueba si el usuario hizo clic en el botón **Cancelar** o presiona la tecla ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Obtiene el identificador de instancia de Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Obtiene el identificador de la ventana principal de Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Obtiene la ruta de acceso y el nombre del archivo DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Esta función está en desuso y ya no necesita que se llame.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Esta función está en desuso y ya no necesita que se llame.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Define un nombre binario de almacenamiento persistente.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Obtiene los datos de un nombre almacenamiento persistente de binarios.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Devolver el valor XLOPER y XLOPER12: operRes

El argumento _operRes_ es el segundo argumento para las devoluciones de llamada y es un puntero a un **XLOPER** (**Excel4** y **Excel4v**) o **XLOPER12** (**Excel12** y **Excel12v**). Después de una llamada correcta, que contiene el valor devuelto de la función o el comando. **operRes** se puede establecer en cero (puntero nulo) si se requiere ningún valor devuelto. Por lo que se debe liberar antes de cualquier memoria previamente que apunta a la llamada a fin de evitar pérdidas de memoria, se sobrescribe el contenido anterior de **operRes** . 
  
Si la función o el comando no se puede llamar (por ejemplo, si los argumentos no están correcta), **operRes** se establece en el error **#VALUE!**. Un comando siempre devuelve **Boolean** **es TRUE** si es correcto, o **FALSE** si se produjo un error o el usuario cancelado. 
  
## <a name="number-of-subsequent-arguments-count"></a>Número de argumentos subsiguientes: count

El argumento _count_ es el tercer argumento para las devoluciones de llamada y es un entero con signo de 32 bits. Se debe establecer el número de argumentos subsiguientes, a partir de 1. Si un comando o función no toma ningún argumento, se debe establecer en cero. En Microsoft Office Excel 2003, el número máximo de argumentos que puede realizar cualquier función es 30, aunque la mayoría toman menos de esto. Iniciar en Excel 2007, el número máximo de argumentos que puede realizar cualquier función se ha aumentado a 255. 
  
Con **Excel4** y **Excel12**, _count_ es el número de punteros a **XLOPER** o **XLOPER12** valores que se pasan. Debe ser muy cuidado de no pase ese _recuento_ de menos argumentos que el valor se establece en. Esto haría en Excel, leer con antelación a la pila e intenta procesar valores **XLOPER** o **XLOPER12** no válidos, lo que podrían provocar un bloqueo de la aplicación. 
  
Con la **Excel4v** y **Excel12v**, _count_ es el tamaño de la matriz de punteros a **XLOPER** o **XLOPER12** valores que se pasa como el argumento final y siguiente. Una vez más, debe ser muy cuidado de no pasar una matriz más pequeña que el _recuento de_ elementos de tamaño, como los límites de la matriz que se va a saturación dará como resultado. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Pasar argumentos a funciones de la API de C

**Excel4** y **Excel12** tendrán longitud variable listas de argumentos, después de _recuento_, que se interpreta como punteros a valores **XLOPER** y **XLOPER12** , respectivamente. **Excel4v** y **Excel12v** toman un solo argumento, después de _recuento_, que es un puntero a una matriz de punteros a valores **XLOPER** en el caso de la **Excel4v**y a los valores de **XLOPER12** en el caso de **Excel12v**.
  
Los formularios de matriz, la **Excel4v** y **Excel12v**, permiten una llamada a la API C de código de forma limpia cuando el número de argumentos es variable. En el ejemplo siguiente se muestra una función que toma una matriz de tamaño variable de números y funciones de hoja de cálculo de Excel a través de la API de C, se utiliza para calcular la suma, promedio, mínima y máxima. 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

Reemplazar las referencias a valores **XLOPER12** con **XLOPER**y **Excel12v** con la **Excel4v**, en el código anterior diese como resultado una función que funcionaría con todas las versiones de Excel. Esta operación de las funciones de Excel **suma**, **promedio**, **MIN**y **MAX** es lo suficientemente simple para que sea más eficaz para ellos el código de C y para evitar la sobrecarga de preparación de los argumentos y la llamada a Excel. Sin embargo, muchas de las funciones de que Excel contiene son más complejos, hacer que este enfoque útil en algunos casos. 
  
El tema [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) proporciona otro ejemplo de trabajar con la **Excel4v** y **Excel12v**. Cuando se registra una función de hoja de cálculo XLL, puede proporcionar una cadena descriptiva para cada argumento que se usa en el cuadro de diálogo **Pegar función** . Por lo tanto, el número de argumentos totales que se proporciona para **xlfRegister** depende del número de argumentos que toma la función XLL y varían en función de una función a la siguiente. 
  
Siempre se llama a una función de la API de C o un comando con el mismo número de argumentos, por lo que desea evitar el paso adicional de la creación de una matriz de punteros para esos argumentos. En esos casos, es más sencillo y más ordenado para usar **Excel4** y **Excel12**. Por ejemplo, cuando se registra los comandos y funciones XLL, debe proporcionar el nombre de archivo y ruta de acceso completo de la DLL o XLL. Puede obtener el nombre de archivo en una llamada a **xlfGetName** y, a continuación, liberar con una llamada a **xlFree**, tal como se muestra en el siguiente ejemplo para **Excel4** y **Excel12**.
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

En la práctica, la función, **Excel12v_example**, podría codificada de forma más eficaz mediante la creación de un único **xltypeMulti** **XLOPER12** argumento y llamar a la API C mediante el uso de **Excel12**, tal como se muestra en el siguiente ejemplo.
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> En este caso, se omite el valor devuelto de **Excel12** . En su lugar, el código comprueba que el devuelto **XLOPER12** es **xltypeNum** para determinar si la llamada se realizó correctamente. 
  
## <a name="xlcallver"></a>XLCallVer

Además de las devoluciones de llamada **Excel4**, **Excel4v**, **Excel12**y **Excel12v**, Excel exporta una función **XLCallVer**, que devuelve la versión de la API de C se está ejecutando actualmente.
  
El prototipo de función es como sigue:
  
 `int pascal XLCallVer(void);`
  
Puede llamar a esta función, que es segura, desde cualquier comando XLL o función de subprocesos.
  
En Excel 97 a Excel 2003, **XLCallVer** devuelve 1280 = 0 x 0500 hex = 5 x 256, que indica la versión 5 de Excel. Iniciar en Excel 2007, devuelve 0x0c00 = 3072 hex = 12 x 256, que indica la versión 12.
  
Aunque se puede usar para determinar si la nueva API de C está disponible en tiempo de ejecución, es posible que prefiera detectar la versión de Excel que se está ejecutando mediante el uso de `Excel4(xlfGetWorkspace, &version, 1, &arg)`, donde `arg` es un valor numérico **XLOPER** establecido en 2. La función devuelve una cadena **XLOPER**, la versión, a continuación, se puede convertir a un número entero. El motivo de la confianza en la versión de Excel en lugar de la versión de la API C es que no hay diferencias entre Excel 2000, Excel 2002 y Excel 2003 que el complemento es posible que también necesite detectar. Por ejemplo, se realizaron cambios en la precisión de algunas de las funciones de estadísticas.
  
## <a name="see-also"></a>Vea también



[Crear XLL](creating-xlls.md)
  
[Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

