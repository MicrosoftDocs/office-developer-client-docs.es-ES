---
title: Llamar a Excel desde el DLL o XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cuadros de diálogo [excel 2007], invocar comandos de excel,DLL [Excel 2007], llamar a Excel,pasar argumentos a funciones API C [Excel 2007],comandos [Excel 2007],invocar con cuadros de diálogo,comandos [Excel 2007],accesibles desde DLL o XLL,función de Excel4,función de Excel12 [Excel 2007],función de XLCallVer [Excel 2007],argumento operRes [Excel 2007],funciones [Excel 2007], accesibles desde DLL o XLL,función de Excel12v [Excel 2007], funciones solo DLL [Excel 2007],API de C [Excel 2007],pasar argumentos,argumento de número [Excel 2007],comandos [Excel 2007], llamar a versiones internacionales, comandos solo DLL [Excel 2007],versiones internacionales [Excel 2007],llamar a funciones y comandos,XLL [Excel 2007], llamar a Excel,función de Excel 4v [ Excel 2007],argumento xlfn [Excel 2007],funciones [Excel 2007], llamar a versiones internacionales
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726123"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Llamar a Excel desde el DLL o XLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel permite que el DLL tenga acceso a comandos de Excel integrados, funciones de hoja de cálculo y funciones de hoja de macros. Están disponibles en los comandos de DLL y las funciones que se llaman desde Visual Basic para Aplicaciones (VBA), así como en las funciones y los comandos XLL registrados que Excel llama directamente.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Funciones de Excel4, Excel4v, Excel12 y Excel12v

Excel permite que el DLL tenga acceso a los comandos y las funciones a través de las funciones de devolución de llamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md) y [Excel12v](excel4v-excel12v.md).
  
Las funciones de **Excel4** y **Excel4v** se introdujeron en la versión 4 de Excel. Trabajar con la estructura de datos **XLOPER**. Excel 2007 introdujo dos nuevas funciones de devolución de llamada, **Excel12** y **Excel12v**, que trabajan con a estructura de datos **XLOPER12**. Las funciones de **Excel4** y **Excel4v** se exportan mediante la biblioteca Xlcall32.lib, que debe incluirse en el proyecto DLL o XLL. **Excel12** y **Excel12v** se incluyen en el archivo de origen del SDK para C++ Xlcall.cpp, el cual debe incluirse en el proyecto si desea obtener acceso a las funciones de Excel mediante estructuras **XLOPER12**. 
  
El siguiente código muestra los prototipos de función para estas cuatro funciones. Los primeros tres argumentos son los mismos, excepto que el segundo argumento es un puntero a una estructura **XLOPER** en el primer par y un puntero a una estructura **XLOPER12** en el segundo par. La convención de llamada es **_cdecl** en **Excel4** y **Excel12** para permitir las listas de argumentos variables. Los puntos suspensivos representan punteros a valores de **XLOPER** para **Excel4** y valores de **XLOPER12** para **Excel12**. El número de punteros es igual al valor del parámetro de _recuento_. 
  
**Todas las versiones de Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**A partir de Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Para que el DLL pueda llamar a **Excel4**, **Excel4v**, **Excel12** o **Excel12v**, Excel debe pasar el control al DLL. Esto significa que es posible llamar a estas devoluciones de llamada de API C únicamente en las siguientes situaciones:
  
- Desde un comando XLL al que Excel llamó directamente o a través de VBA.
    
- Desde una hoja de cálculo XLL o una función de hoja de macros que Excel llamó directamente o a través de VBA.
    
No puede llamar a la API C de Excel en las siguientes situaciones:
  
- Desde un evento de sistema operativo (por ejemplo, desde la función [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)). 
    
- Desde un proceso en segundo plano que haya creado el DLL.
    
### <a name="return-values"></a>Valores devueltos

Las cuatro funciones devuelven un valor entero que informa al autor de llamada si fue posible llamar correctamente a la función o al comando. Los valores devueltos pueden ser uno de los siguientes:
  
|**Valor devuelto**|**Definido en Xlcall.h como**|**Descripción**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La función o el comando se ejecutaron correctamente. Esto no significa que la ejecución haya estado exenta de errores. Por ejemplo, **Excel4** pudo devolver **xlretSuccess** cuando llamó a la función **FIND**, aunque la evaluó como **#VALUE!** porque no se encontró el texto de búsqueda. Es necesario inspeccionar el tipo y el valor devuelto **XLOPER o XLOPER12** cuando es posible.  <br/> |
|1  <br/> |**xlretAbort** <br/> |El usuario detuvo una macro de comando al hacer clic en el botón **CANCELAR** o presionar la tecla ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |El código de comando o la función especificada no es válida. Este error puede ocurrir cuando la función de llamada no tiene permiso para llamar a la función o el comando. Por ejemplo, una función de hoja de cálculo no puede llamar a una función de comando o una función de información de hoja de macros.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |El número de argumentos proporcionados en la llamada no es correcto.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Uno o más de los valores del argumento **XLOPER** o **XLOPER12** no están formados o rellenados correctamente.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel detectó un riesgo en la operación de desbordamiento de su pila y, por lo tanto, no llamó a la función.  <br/> |
|32  <br/> |**xlretFailed** <br/> |Se produjo un error en el comando o la función por un motivo que no se describe en uno de los demás valores devueltos. Una operación que necesita una gran cantidad de memoria, por ejemplo, podría generar este error. Esto puede ocurrir durante un intento de convertir una enorme referencia en una matriz **xltypeMulti** mediante la función [xlCoerce](xlcoerce.md).  <br/> |
|64  <br/> |**xlretUncalced** <br/> |La operación intentó recuperar el valor de una celda no actualizada. Para mantener la integridad de actualización de Excel, no se permite que las funciones de la hoja de cálculo lo hagan. Sin embargo, las funciones y los comandos XLL registrados como funciones de hoja de macros puedan obtener acceso a los valores de celdas no actualizadas.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(A partir de Excel 2007) Una función de hoja de cálculo XLL registrada como segura para subprocesos intentó llamar a una función de la API de C que no es segura para subprocesos. Por ejemplo, una función segura para subprocesos no puede llamar a la función XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(A partir de Excel 2010) El controlador de la función asincrónica no es válido.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(A partir de Excel 2010) No se admite la llamada en clústeres.  <br/> |
   
Si la función devuelve uno de los valores de error en la tabla (es decir, no devuelve **xlretSuccess**), el valor devuelto **XLOPER** o **XLOPER12** también se establecerá en **#VALUE!**. En determinadas circunstancias, comprobarlo puede ser una prueba suficiente de éxito, pero tenga en cuenta que una llamada puede devolver tanto **xlretSuccess** como **#VALUE!**.
  
Si una llamada a la API C da como resultado **xlretUncalced** o **xlretAbort**, el código de DLL o XLL debe devolver control a Excel antes de realizar cualquier otra llamada a la API C (además de las llamadas a la función [xlfree ](xlfree.md) para liberar recursos de memoria asignados a Excel en los valores **XLOPER** y **XLOPER12**). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Argumento de enumeración de funciones o comandos: xlfn

El argumento _xlfn_ es el primer argumento de las funciones de devolución de llamada y es un entero con signo de 32 bits. El valor debe ser una de las enumeraciones de comandos o funciones definidas en el archivo de encabezado del SDK Xlcall.h, tal como se muestra en el siguiente ejemplo. 
  
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

Todas las funciones de la hoja de macros y la hoja de cálculo están comprendidas entre 0 (**xlfCount**) y 0x0fff hexadecimal, aunque el mayor número asignado en Excel 2013 es 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).
  
Todas las funciones de comandos están comprendidas entre 0x8000 hexadecimal (**xlcBeep**) y 0x8fff hexadecimal, aunque el mayor número asignado en Excel 2013 es 0x8328 hexadecimal (**xlcHideallInkannots**). Se definen en el archivo de encabezado como `(n | xlCommand)`, donde `n` es un número decimal mayor o igual que 0 y **xlCommand** se define como 0x8000 hexadecimal. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Invocar comandos de Excel que usan cuadros de diálogo

Algunos de los códigos de comando corresponden a las acciones en Excel que usan cuadros de diálogo. Por ejemplo, **xlcFileDelete** toma un solo argumento: un nombre de archivo o una máscara. Esto se puede invocar con el cuadro de diálogo para que el usuario tenga la oportunidad de cancelar o modificar la operación de eliminación. También se puede llamar sin el cuadro de diálogo, en cuyo caso el archivo o los archivos se eliminan sin mayor interacción, suponiendo que existen y que al autor de llamada tiene permiso. Para llamar a estos comandos en su forma de cuadro de diálogo, la enumeración de comandos debe combinarse mediante la operación bit a bit OR con 0x1000 (**xlPrompt**).
  
El siguiente ejemplo de código elimina archivos en el directorio actual que coinciden con la máscara my_data\*.bak y muestra un cuadro de diálogo solo si el argumento es verdadero.
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a>Llamar a funciones y comandos en versiones internacionales

Puede configurar Excel para mostrar los nombres de comandos XLM y funciones en varios idiomas. Algunas funciones y comandos de la API de C operan en cadenas que se interpretan como nombres de comandos o funciones. Por ejemplo, **xlcFormula** acepta un argumento de cadena que está pensado para colocarse en una celda especificada. Para que el complemento funcione con todas las opciones de idioma, puede proporcionar los nombres de la cadena en inglés y establecer el bit 0x2000 (**xlIntl**) en la enumeración de comandos o funciones.
  
En el siguiente ejemplo de código se coloca el equivalente a `=SUM(X1:X100)` en la celda A2 de la hoja activa. Tenga en cuenta que se usa la función Framework, **TempActiveRef**, para crear una referencia externa temporal **XLOPER**. La fórmula aparecerá en A2 en el idioma correcto determinado por la configuración regional (por ejemplo, `=SOMME(X1:X100)` si el idioma es francés). 
  
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
> Como el resultado de la llamada a **Excel12** no es necesario, podría pasarse cero (NULL) como segundo argumento en lugar de la dirección de **xResult**. Esto se describe con más detalle en la siguiente sección. 
  
### <a name="dll-only-functions-and-commands"></a>Comandos y funciones solo de DLL

Excel admite un número reducido de funciones que solo son accesibles desde un DLL o XLL. Se definen en el archivo de encabezado como `(n | xlSpecial)`, donde `n` es un número decimal mayor o igual que 0 y `xlSpecial` se define como 0x4000 hexadecimal. Estas funciones se enumeran en la siguiente tabla y se documentan en la [Referencia de la función de API](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Libera los recursos de memoria asignados por Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Devuelve el espacio disponible en la pila de Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Convierte entre tipos de **XLOPER** y **XLOPER12**  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Proporciona un método rápido para establecer los valores de celda.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Obtiene un nombre de hoja de cálculo a partir de su identificador interno.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Obtiene un identificador interno de hoja de cálculo a partir de su nombre.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Comprueba si el usuario hizo clic en el botón **CANCELAR** o presionó la tecla ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Obtiene el identificador de instancia de Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Obtiene el identificador de ventana principal de Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Obtiene la ruta de acceso y el nombre de archivo del DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Esta función está en desuso y ya no es necesario llamarla.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Esta función está en desuso y ya no es necesario llamarla.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Define un nombre de almacenamiento binario permanente.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Obtiene datos de un nombre de almacenamiento binario permanente.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Devuelve el valor XLOPER o XLOPER12: operRes

El argumento _operRes_ es el segundo argumento para las devoluciones de llamadas y es un puntero a un **XLOPER** (**Excel4** y **Excel4v**) o ** XLOPER12** (**Excel12** y **Excel12v**). Después de una llamada correcta, contiene el valor devuelto de la función o el comando. **operRes** puede establecerse en cero (puntero nulo) si no se requiere ningún valor devuelto. El contenido anterior de **operRes** se sobrescribe para poder liberar antes toda la memoria a la que se apuntó previamente a fin de evitar pérdidas de memoria en la llamada. 
  
Si no es posible llamar a la función o el comando (por ejemplo, si los argumentos son incorrectos), **operRes** se establece en el error **#VALUE!**. Un comando siempre devuelve un valor **booleano** **TRUE** si funciona correctamente o **FALSE** si se produjo un error o el usuario lo canceló. 
  
## <a name="number-of-subsequent-arguments-count"></a>Número de argumentos siguientes: count

El argumento _count_ es el tercer argumento de las devoluciones de llamada y es un entero con signo de 32 bits. Se debe establecer en el número de argumentos siguientes, a partir de 1. Si un comando o una función no recibe argumentos, debe establecerse en cero. En Microsoft Office Excel 2003, el número máximo de argumentos que puede recibir cualquier función es 30, aunque la mayoría reciben menos. A partir de Excel 2007, se aumenta el número máximo de argumentos que puede recibir cualquier función a 255. 
  
Con **Excel4** y **Excel12**, _count_ es el número de punteros a los valores **XLOPER** o **XLOPER12** que se pasan. Debe tener cuidado de no a pasar menos argumentos que el valor en el que se establece _count_. Esto provocaría que Excel siga leyendo en la pila e intente procesar valores **XLOPER** o **XLOPER12** no válidos, lo que podría bloquear la aplicación. 
  
Con **Excel4v** y **Excel12v**, _count_ es el tamaño de la matriz de punteros a los valores **XLOPER** o **XLOPER12** que se pasan como el argumento siguiente y final. De nuevo, debe tener cuidado de no pasar una matriz menor que _count_ elementos en tamaño, ya que esto provocará la saturación de los límites de la matriz. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Pasar argumentos a las funciones de la API de C

Tanto **Excel4** como **Excel12** toman listas de argumentos de longitud variable, después de _count_, que se interpretan como punteros a los valores **XLOPER** y **XLOPER12**, respectivamente. **Excel4v** y **Excel12v** reciben un solo argumento, después de _count_, que es un puntero a una matriz de punteros a los valores **XLOPER** en el caso de **Excel4v** y a los valores **XLOPER12** en el caso de **Excel12v**.
  
Los formularios de matriz, **Excel4v** y **Excel12v**, le permiten programar una llamada a la API de C de forma nítida cuando el número de argumentos es variable. El siguiente ejemplo muestra una función que toma una matriz de números de tamaño variable y usa las funciones de hoja de cálculo de Excel, mediante la API de C, para calcular la suma, el promedio, el mínimo y el máximo. 
  
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

Reemplazar las referencias a los valores **XLOPER12** con **XLOPER** y **Excel12v** con **Excel4v**, en el código anterior tendría como resultado una función compatible con todas las versiones de Excel. Esta operación de las funciones de Excel **SUMA**, **PROMEDIO**, **MIN** y **MÁX** es bastante sencilla por lo que sería más eficaz programarlas en C y evitar la sobrecarga de preparar los argumentos y llamar a Excel. Sin embargo, muchas de las funciones que contiene Excel son más complejas, por lo que este método es útil en algunos casos. 
  
El tema sobre [xlfRegister](xlfregister-form-1.md) proporciona otro ejemplo de trabajo con **Excel4v** y **Excel12v**. Cuando se registra una función de hoja de cálculo XLL, puede proporcionar una cadena descriptiva para cada argumento que se usa en el cuadro de diálogo **Pegar función**. Por lo tanto, el número de argumentos totales que se proporciona a **xlfRegister** depende del número de argumentos que acepta la función XLL y puede variar de una función a otra. 
  
Si siempre llama a una función de la API de C o un comando con el mismo número de argumentos, querrá evitar el paso adicional de la creación de una matriz de punteros para esos argumentos. En esos casos, es más sencillo y más claro usar **Excel4** y **Excel12**. Por ejemplo, al registrar los comandos y las funciones XLL, debe proporcionar la ruta de acceso completa y el nombre de archivo del DLL o XLL. Puede obtener el nombre de archivo en una llamada a **xlfGetName** y después liberarlo con una llamada a **xlFree**, tal como se muestra en el ejemplo siguiente para **Excel4** y ** Excel12**.
  
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

En la práctica, la función **Excel12v_example**, podría codificarse de forma más eficiente creando un solo argumento **xltypeMulti** **XLOPER12** y llamando a la API de C mediante **Excel12**, tal como se muestra en el ejemplo siguiente.
  
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
> En este caso, el valor devuelto de **Excel12** se pasa por alto. En su lugar, el código comprueba que el valor **XLOPER12** devuelto sea **xltypeNum** para determinar si la llamada se realizó correctamente. 
  
## <a name="xlcallver"></a>XLCallVer

Además de las devoluciones de llamada a **Excel4**, **Excel4v**, **Excel12** y **Excel12v**, Excel exporta una función ** XLCallVer**, que devuelve la versión de la API de C actualmente en ejecución.
  
El prototipo de la función es el siguiente:
  
 `int pascal XLCallVer(void);`
  
Puede llamar a esta función, que es segura para subprocesos, desde cualquier función o comando XLL.
  
En Excel 97 a Excel 2003, **XLCallVer** devuelve 1280 = 0x0500 hex = 5 x 256, que indica la versión 5 de Excel. A partir de Excel 2007, devuelve 3072 = 0x0c00 hex = 12 x 256, que asimismo indica la versión 12.
  
Aunque puede usar esto para determinar si la nueva API de C está disponible en tiempo de ejecución, tal vez prefiera detectar la versión en ejecución de Excel mediante `Excel4(xlfGetWorkspace, &version, 1, &arg)`, donde `arg` es un valor **XLOPER** numérico que se establece en 2. La función devuelve una cadena **XLOPER**, versión, que después puede convertirse en un entero. Las razones para depender de la versión de Excel en lugar de la versión de la API de C es que hay diferencias entre Excel 2000, Excel 2002 y Excel 2003 que tal vez el complemento necesite detectar también. Por ejemplo, los cambios realizados en la precisión de algunas de las funciones estadísticas.
  
## <a name="see-also"></a>Vea también

- [Crear XLL](creating-xlls.md)  
- [Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)  
- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)  
- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

