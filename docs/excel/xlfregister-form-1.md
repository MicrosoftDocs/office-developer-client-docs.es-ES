---
title: xlfRegister (Formulario 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303867"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formulario 1)

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde un comando DLL o XLL a los que ha llamado Microsoft Excel. Es igual a llamar a **Register** desde una hoja de macros XLM de Excel. 
  
se puede llamar a **xlfRegister** de dos formas: 
  
- xlfRegister (formulario 1): registra un único comando o función.
    
- [xlfRegister (formulario 2)](xlfregister-form-2.md): carga y activa un XLL.
    
Llamada en el formulario 1, esta función hace que una función o un comando DLL esté disponible en Excel, establece su recuento de uso en 1 y devuelve su identificador de registro, que se puede usar para llamar a la función más adelante mediante la función [xlUDF](xludf.md) o **xlfCall** . El identificador de registro también se usa para anular el registro de la función con [xlfUnregister (formulario 1)](xlfunregister-form-1.md). Si se ha registrado la función, al llamar a **xlfRegister** , se incrementa su recuento de uso. 
  
Esta forma de la función también define un nombre oculto que es el argumento del texto de la función, _pxFunctionText_, y que se evalúa en el identificador de registro de la función o el comando. Al anular el registro de la función, elimine este nombre con el [xlfSetName](xlfsetname.md). Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
El nombre de la DLL que contiene la función. Esto se puede obtener si se llama a la función solo XLL [xlGetName](xlgetname.md) si la función registrada también está dentro de la dll que se está ejecutando actualmente. 
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si es una cadena, el nombre de la función a la que se llama como aparece en el código DLL. Si es un número, el número de exportación ordinal de la función que se va a llamar. Para mayor claridad, use siempre el formulario de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de argumentos de la función y el tipo de valor devuelto de la función. Para obtener más información, vea la sección Comentarios. Este argumento puede omitirse para una DLL independiente (XLL) que incluya una [función xlAutoRegister](xlautoregister-xlautoregister12.md) o **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** solo se admite en Excel 2007. 
  
Si se llama a **xlfRegister** con este argumento que falta, Excel llama a **xlAutoRegister** o **xlAutoRegister12**, si existe en la dll especificada, que debe registrar la función correctamente proporcionando esta información.
  
_pxFunctionText_ (**xltypeStr**)
  
El nombre de la función tal y como aparecerá en el Asistente para funciones. Este argumento es opcional; Si se omite, la función no está disponible en el Asistente para funciones y solo se puede llamar mediante la función **Call** mediante el identificador de registro de funciones de una hoja de macros XLM. Por lo tanto, para el uso de la hoja de cálculo normal, debe controlar este argumento según sea necesario. 
  
_pxArgumentText_ (**xltypeStr**)
  
Cadena de texto opcional que describe los argumentos de la función. El usuario lo ve en el Asistente para funciones. Si se omite, Excel crea descripciones básicas desde _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** o **xltypeInt**)
  
Argumento opcional que indica el tipo de punto de entrada XLL. El valor predeterminado, si se omite, es 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valor pxMacroType_ <br/> |comprendi  <br/> |1  <br/> |segundo  <br/> |
|Se puede llamar desde una hoja de cálculo  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se puede llamar desde una hoja de macros.  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se puede llamar desde una definición de nombre definida  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se puede llamar desde una expresión de formato condicional  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Enumerados en el Asistente para funciones para funciones de hoja de cálculo  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Enumerados en el Asistente para funciones para funciones de hoja de macros  <br/> |No  <br/> |Sí  <br/> |Sí  <br/> |
   
En la práctica, debe usar 1 para las funciones de hoja de cálculo, 1 para las funciones equivalentes **#** de la hoja de macros (registradas como tipo) a las que desea llamar desde la hoja de cálculo y 2 para los comandos. 
  
> [!NOTE]
> Los comandos XLL están ocultos y no se muestran en los cuadros de diálogo para ejecutar macros, aunque se pueden escribir sus nombres en cualquier lugar donde se necesite un nombre de comando válido. 
  
_pxCategory_ (**xltypeStr** o **xltypeNum**)
  
Un argumento opcional que permite especificar la categoría a la que debe pertenecer la función o el comando nuevos. El Asistente para funciones divide las funciones por tipo (categoría). Puede especificar un nombre de categoría o un número secuencial, donde el número es la posición en la que aparece la categoría en el Asistente para funciones. Para obtener más información, consulte la sección "nombres de categorías". Si se omite, se asume la categoría definida por el usuario.
  
_pxShortcutText_ (**xltypeStr**)
  
Cadena de un carácter, con distinción entre mayúsculas y minúsculas que especifica la tecla de control asignada a este comando. Por ejemplo, "A" asigna este comando a CONTROL + Mayús + A. Este argumento es opcional y se usa solo para comandos.
  
_pxHelpTopic_ (**xltypeStr**)
  
Una referencia opcional al archivo de ayuda (. chm o. hlp) que se muestra cuando el usuario hace clic en el botón ayuda (cuando se muestra la función personalizada). Puede tener el formato `filepath!HelpContextID` o. `https://address/path_to_file_in_site!0` Se requieren las dos partes antes y después de la "!".  *HelpContextID* no debe contener comillas simples y Excel se convertirá en un entero sin signo de 4 bytes de longitud, en forma decimal. Cuando se usa el formulario de dirección URL, Excel abre sólo el archivo de ayuda al que se hace referencia. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Una cadena opcional que describe la función personalizada cuando se selecciona en el Asistente para funciones.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Opcional. Primera de las cadenas que describen los argumentos personalizados de la función cuando la función está seleccionada en el Asistente para funciones. En Excel 2003 y versiones anteriores, **xlfRegister** puede tardar, como máximo, 30 argumentos para que pueda proporcionar esta ayuda solo para los primeros 20 de los argumentos de la función. A partir de Excel 2007, **xlfRegister** puede tardar hasta 255 argumentos para que pueda proporcionar esta ayuda para un máximo de 245 parámetros de función. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si el registro se realizó correctamente, esta función devuelve el identificador de registro de la función (**xltypeNum**), que se puede usar en las llamadas a **xlUDF** y **xlfUnregister** en un archivo dll, o bien con **llamar** y **anular el registro** en una hoja de macros XLM. De lo contrario, devuelve un #VALUE! error. 
  
## <a name="remarks"></a>Comentarios

### <a name="data-types"></a>Tipos de datos

El argumento _pxTypeText_ especifica el tipo de datos del valor devuelto y los tipos de datos de todos los argumentos de la función de dll o recurso de código. El primer carácter de _pxTypeText_ especifica el tipo de datos del valor devuelto. Los caracteres restantes indican los tipos de datos de todos los argumentos. Por ejemplo, una función DLL que devuelve un número de punto flotante y toma un entero y un número de punto flotante como argumentos requeriría "BIB" para el argumento _pxTypeText_ . 
  
Las estructuras y los tipos de datos que usa Excel para intercambiar datos con los XLL se resumen en las dos tablas siguientes.
  
En la primera tabla se enumeran los tipos compatibles con todas las versiones de Excel.
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Booleano  <br/> |A  <br/> |L  <br/> |Short [int] (0 = false o 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*   <br/> ||C, F  <br/> |Cadena de bytes en ASCII terminada en null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadena de bytes ASCII contados  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD de 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |entero con signo de 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |entero con signo de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Estructura de matriz con punto flotante  <br/> |
|Matriz  <br/> ||O  <br/> |Se pasan tres argumentos:<br/>-unsigned short int\*<br/>-unsigned short int\*<br/>-Double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||R  <br/> |Referencias de rango, matrices y valores  <br/> |
   
En Excel 2007, se introdujeron los siguientes tipos de datos para admitir las cuadrículas más grandes y cadenas Unicode largas.
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|unsigned short\*  <br/> ||C%, F%  <br/> |Cadena de caracteres anchos Unicode terminada en null  <br/> |
|unsigned short\*  <br/> ||D%, G%  <br/> |Cadena de caracteres anchos Unicode contada  <br/> |
|FP12  <br/> ||K%  <br/> |Estructura de matriz de punto flotante de cuadrícula más grande  <br/> |
|Matriz  <br/> ||O%  <br/> |Se pasan tres argumentos:<br/>-signed int \* /RW\*<br/>-signed int \* /col\*<br/>-Double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||U  <br/> |Referencias de rango, matrices y valores  <br/> |
   
A partir de Excel 2010, se introdujeron los siguientes tipos de datos:
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |El identificador asincrónico se usa para realizar un seguimiento de una llamada a una función asincrónica pendiente que Excel y el XLL. La existencia del tipo de parámetro en la cadena de tipo también designa la función como asincrónica. Para obtener más información acerca de las funciones asincrónicas, consulte [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).  <br/> |
   
Los tipos de cadena **F**, **F%**, **G**, y **G%** se usan para los argumentos modificados en sitio.  
  
Al trabajar con los tipos de datos mostrados en la tabla anterior, tenga en cuenta lo siguiente:
  
- Las declaraciones de lenguaje C suponen que el compilador usa dobles de 8 bytes, enteros cortos de 2 bytes y enteros largos de 4 bytes de forma predeterminada.
    
- Todas las funciones de dll y los recursos de código se llaman mediante la Convención de llamada **_ _ Stdcall** . 
    
- Cualquier función que devuelve un tipo de datos por referencia, es decir, que devuelve un puntero a algo, puede devolver de forma segura un puntero nulo. Excel interpreta un puntero nulo como #NUM! error.
    
## <a name="additional-data-type-information"></a>Información de tipo de datos adicional

Esta sección contiene información detallada sobre los tipos de datos **E**, **f**, **f%**, **g**, **g%**, **K**, **O**, **P**, **Q**, **R**y **U** , y otra información sobre el _pxTypeText _argumento. 
  
### <a name="e-data-type"></a>Tipo de datos E

Excel espera que una DLL que usa el tipo de datos E pase punteros a números de punto flotante en la pila. Esto puede causar problemas con algunos idiomas (por ejemplo, Borland C++) que esperan que el número se pase en la pila del emulador del coprocesador. La solución alternativa es pasar un puntero al número en la pila del coprocesador. En el ejemplo siguiente se muestra cómo devolver un doble de Borland C++.
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>Tipos de datos F, F%, G y G%

Con los tipos de datos **f**, **f%**, **g**y **g%** , una función puede modificar un búfer de cadena asignado por Excel. Si el tipo de valor devuelto es uno de estos tipos, Excel omite el valor devuelto por la función. En su lugar, Excel busca en la lista de argumentos de función el primer tipo de datos correspondiente (**f**, **f%**, **g**o **g%**) y, a continuación, toma el contenido actual del búfer de cadena asignado como el valor devuelto. Todas las versiones de Excel asignan 256 bytes para las cadenas **F** y **G** ASCII, y a partir de Excel 2007 65.536 bytes se asignan lo suficiente para 32.768 caracteres Unicode para las cadenas Unicode de **F%** y **G%** . Recuerde que los búferes deben incluir un carácter de recuento (Types **g** y **g%**) o un carácter de terminación null (tipos **F** y **f%**), de modo que las longitudes de cadena máximas son 255 y 32.767. Las cadenas Unicode y, por tanto, los argumentos de los tipos **F%** y **G%** , solo están disponibles a través de la API de C en Excel. 
  
### <a name="k-and-k-data-types"></a>Tipos de datos K y K%

Los tipos de datos **k** y **k%** utilizan punteros a las estructuras FP y FP12 de tamaño variable, respectivamente. Estas estructuras están definidas en XLLCALL. H. Las estructuras FP12 y, por lo tanto, los argumentos de tipo **K%** , solo se admiten a partir de Excel 2007. 
  
### <a name="o-and-o-data-types"></a>Tipo de datos O o O

Los tipos de datos de **o** o **o%** solo se pueden usar para argumentos, no valores devueltos, aunque se puede devolver valores **** que modifiquen un argumento de tipo de **%** de o o o en su lugar. Cada una de ellas pasa tres elementos: un puntero al número de filas de una matriz, un puntero al número de columnas de una matriz y un puntero a una matriz bidimensional de números de punto flotante. 
  
Para modificar una matriz pasada por el tipo de datos o o o de% en su ubicación, puede usar ">O" o ">O%" como el argumento _pxTypeText_ . Para obtener más información acerca de la modificación de una matriz, vea la sección "modificar en la ubicación: funciones deClaradas como Void" de este tema. 
  
El tipo de datos **O** se ha creado para ofrecer compatibilidad directa con los archivos dll Fortran, que pasan argumentos por referencia. 
  
El **O%** es compatible a partir de Excel 2007 y acomoda el mayor número de filas que admite Excel. 
  
### <a name="p-and-q-data-types"></a>Tipos de datos P y Q

Cuando los argumentos de la función DLL están registrados como toma de tipo **p** XLOPER o de tipo **Q** xloper12, Excel convierte las referencias de una sola celda en valores simples y las referencias de varias celdas a matrices al preparar estos argumentos. En otras palabras, los tipos **p** y **Q** siempre recibirán en la función como uno de estos tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**o **xltypeNil **, pero no **XltypeRef** ni **xltypeSRef** porque siempre se les ha desreferenciado. Los **XLOPER12**s y, por lo tanto, los argumentos de tipo **Q** , solo se admiten a partir de Excel 2007. 
  
Si los tipos **xltypeMissing** o **xltypeNil** se usan para los valores devueltos, Excel los interpreta como Numeric cero. **xltypeMissing** se pasa cuando el autor de la llamada omite un argumento. **xltypeNil** se pasa cuando el autor de la llamada pasa una referencia a una celda vacía. Cuando un rango de celdas se convierte en un **xltypeMulti** que se va a pasar como tipo **P** o **Q**, todas las celdas en blanco dentro del rango se convierten en elementos de la matriz **xltypeNil** . Los elementos que faltan en una matriz literal se pasan de manera similar como elementos **xltypeNil** . 
  
### <a name="volatile-functions-and-recalculation"></a>Funciones volátiles y actualización

En una hoja de cálculo, puede hacer que una función de DLL o un recurso de código sea volátil, de modo que se vuelvan a calcular cada vez que se actualice la hoja de cálculo. Para ello, agregue un signo de exclamación (!) después del último código de argumento en el argumento _pxTypeText_ . 
  
> [!NOTE]
> De forma predeterminada, las funciones que toman el tipo **R** XLOPER o el tipo **U** xloper12 y que están registradas como equivalentes de hoja de macros (tipo **#**; vea la sección siguiente) se administran como volátiles en Excel. 
  
### <a name="functions-declared-as-void"></a>Funciones declaradas como void

Hay dos casos en los que se llama a declarar una función como que devuelve void. En ambos casos, la función devuelve el resultado por otros medios.
  
#### <a name="modifying-in-place"></a>Modificación local

Puede usar un único dígito _n_ para el código de tipo devuelto en _pxTypeText_, donde _n_ es un número del 1 al 9. Esto indica a Excel que tome el valor de la variable en la ubicación a la que apunta el argumento _n_th en _pxTypeText_ como el valor devuelto. Esto también se conoce como modificación local. El argumento _n_th debe ser un tipo de datos de paso por referencia (C, D, E, F, F%, G, G%, K, K%, L, M, N, o, O%, P, p, R o U). La función de DLL o el recurso de código también deben declararse con la palabra clave **void** en los lenguajes C/C++ (o la palabra clave **procedure** en el lenguaje Pascal). 
  
Por ejemplo, una función DLL que toma una cadena terminada en NULL y dos punteros a enteros como argumentos pueden modificar la cadena en su lugar. Use "1FMM" como argumento _pxTypeText_ y declare la función como void. 
  
Las versiones anteriores de Excel **\>** se usaban al principio de _pxTypeText_ para indicar que la función se declaró como void y que se modificó el primer argumento en su lugar; no había forma de modificar ningún argumento que no sea el primero. El **\>** es equivalente a _n_ = 1 en las versiones de Excel actuales y este **\>** uso de funciones sincrónicas solo se admite por compatibilidad con versiones anteriores. 
  
#### <a name="asynchronous-functions"></a>Funciones asincrónicas

Una función asincrónica, que se denota con un parámetro de tipo X en **pxTypeText**, no devuelve el resultado de la llamada de función inicial. En su lugar, debe declarar una función asincrónica como void y, más adelante, el complemento devuelve el resultado mediante una devolución de llamada. La función asincrónica debe registrarse usando **\>** al principio de **pxTypeText**. En las funciones asincrónicas **\>** , denota que la función se declara como void, pero no indica que el primer argumento se modifique en su lugar. Para obtener más información acerca de las funciones asincrónicas, consulte [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrar funciones de hoja de cálculo como equivalentes de hojas de macros (controlar celdas no calculadas)

Colocar un **#** carácter después del último código de parámetro en _pxTypeText_ da a la función los mismos permisos de llamada que las funciones en una hoja de macros. Son las siguientes: 
  
- La función puede recuperar los valores de las celdas que todavía no se han calculado en este ciclo de recálculo.
    
- La función puede llamar a cualquiera de las funciones de información XLM (clase 2), por ejemplo, **xlfGetCell**.
    
- Si el signo de número (#) no está presente: si se evalúa una celda no actualizada, se produce un error **xlretUncalced** y se llama de nuevo a la función actual una vez que se ha calculado la celda; Si se llama a cualquier función de información XLM que no sea **xlfCaller** , se produce un error **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrar funciones de hoja de cálculo como seguras para subprocesos

A partir de Excel 2007, Excel puede realizar cálculos de libros multiproceso. Esto significa que puede asignar distintas instancias de una función segura para subprocesos a subprocesos simultáneos para su reevaluación. A partir de Excel 2007, la mayoría de las funciones integradas de la hoja de cálculo son seguras para subprocesos. A partir de Excel 2007, Excel también permite que los XLL registren funciones de hoja de cálculo como seguras para subprocesos. Para ello, incluya un **$** carácter después del último código de parámetro en _pxTypeText_. 
  
> [!NOTE]
> Solo las funciones de hoja de cálculo pueden declararse como seguras para subprocesos. Excel no considera una función equivalente de hoja de macros para que sea segura para subprocesos, por **#** lo **$** que no se pueden anexar los dos caracteres y al argumento _pxTypeText_ . 
  
Si ha registrado una función como segura para subprocesos, debe asegurarse de que se comporta de un modo seguro para subprocesos, aunque Excel rechace cualquier llamada no segura para subprocesos a través de la API de C. Por ejemplo, si una función segura para subprocesos intenta llamar a **xlfGetCell**, la llamada produce el error **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrar funciones de hoja de cálculo como seguras para clústeres

A partir de Excel 2010, Excel puede descargar llamadas de función a un proveedor de clústeres de cómputo designado. Para obtener más información, consulte [funciones seguras](cluster-safe-functions.md)para clústeres. Las funciones de hoja de cálculo XLL registradas como seguras para clústeres se descargan si un clúster está disponible. Las funciones seguras para clústeres se registran **&amp;** incluyendo el carácter que hay detrás del último código de parámetro en el argumento _pxTypeText_ . 
  
Si ha registrado una función como segura para clústeres, debe asegurarse de que se comporta de manera segura para clústeres. Para obtener más información, consulte [funciones seguras](cluster-safe-functions.md)para clústeres.
  
> [!NOTE]
> Solo las funciones de hoja de cálculo pueden declararse como seguras para clústeres. Excel no considera una función equivalente de hoja de macros para que sea segura para clústeres, por lo **#** que **&amp;** no se pueden anexar los dos caracteres y al argumento _pxTypeText_ . Las funciones de hoja de cálculo pueden declararse como seguras para clústeres y seguras para subprocesos. En este caso, Excel permitirá que estas funciones participen en el recálculo multiproceso cuando la descarga de clústeres está deshabilitada. 
  
### <a name="category-names"></a>Nombres de categoría

Use las siguientes instrucciones para determinar en qué categoría deben colocarse las funciones XLL.
  
- Si la función hace algo que el usuario pueda realizar como parte de la interfaz de usuario del complemento, debe colocar la función en la categoría **comandos** . 
    
- Si la función devuelve información sobre el estado del complemento o cualquier otra información útil, debe colocar la función en la categoría de **información** . 
    
- Un complemento nunca debe agregar funciones ni comandos a la categoría **definida por el usuario** . Esta categoría es para uso exclusivo de usuarios finales. 
    
La categoría se especifica con el parámetro _pxCategory_ en **xlfRegister**. Puede ser un número o texto que corresponda a una de las categorías estándar codificadas de forma rígida o el texto de una nueva categoría especificada por el archivo DLL. Si el texto proporcionado todavía no existe, Excel crea una nueva categoría con ese nombre.
  
En la siguiente tabla se enumeran las categorías estándar que están visibles al ver el cuadro de diálogo **pegar función** desde una hoja de cálculo. 
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Financieras  <br/> |
|segundo  <br/> |Fecha &amp; y hora  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4  <br/> |Texto  <br/> |
|2,5  <br/> |Lógicas  <br/> |
|6,5  <br/> |Lookup &amp; Reference  <br/> |
|0,7  <br/> |Database  <br/> |
|8,5  <br/> |Estadísticas  <br/> |
|9  <br/> |Información  <br/> |
|apartado  <br/> |Definidas por el usuario  <br/> |
||Ingeniería (a partir de Excel 2007)  <br/> |
||Cubo (a partir de Excel 2007)  <br/> |
   
Además, estas categorías también están visibles al ver el cuadro de diálogo **pegar función** desde una hoja de macros. 
  
|**Number**|**Text**|
|:-----|:-----|
|metros  <br/> |Comandos  <br/> |
|12  <br/> |DDE/Externas  <br/> |
|12  <br/> |Personalización  <br/> |
|apartado  <br/> |Control de macros  <br/> |
   
### <a name="example"></a>Ejemplo

Consulte el código de la función **xlAutoOpen** en `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Vea también

- [REGISTER.ID](xlfregisterid.md)
- [ANULAR el registro](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

