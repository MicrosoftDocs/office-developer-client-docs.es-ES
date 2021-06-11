---
title: xlfRegister (Formulario 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfregister [excel 2007]
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
  
Se puede llamar desde un comando DLL o XLL al que ha llamado Microsoft Excel. Esto es igual a llamar a **REGISTER** desde una Excel de macros XLM. 
  
**xlfRegister** se puede llamar de dos formas: 
  
- xlfRegister (formulario 1): registra un único comando o función.
    
- [xlfRegister (formulario 2):](xlfregister-form-2.md)carga y activa un XLL.
    
Llamada en el formulario 1, esta función pone una función DLL o un comando disponible para Excel, establece su recuento de uso en 1 y devuelve su identificador de registro, que se puede usar para llamar a la función más adelante mediante el [xlUDF](xludf.md) o la **función xlfCall.** El identificador de registro también se usa para anular el registro de la función mediante [xlfUnregister (formulario 1).](xlfunregister-form-1.md) Si la función se ha registrado, llamar **a xlfRegister** incrementa de nuevo su recuento de uso. 
  
Esta forma de la función también define un nombre oculto que es el argumento de texto de la función,  _pxFunctionText_, y que se evalúa como el identificador de registro de la función o comando. Al anular el registro de la función, elimine este nombre con [el xlfSetName](xlfsetname.md). Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
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
  
Nombre de la DLL que contiene la función. Esto se puede obtener llamando a la función xLL-only [xlGetName](xlgetname.md) si la función registrada también está dentro del DLL que se está ejecutando actualmente. 
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si se trata de una cadena, el nombre de la función a la que se llamará tal como aparece en el código DLL. Si es un número, el número de exportación ordinal de la función a la que se debe llamar. Para mayor claridad, use siempre el formulario de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de argumentos de la función y el tipo del valor devuelto de la función. Para más información, vea la sección Observaciones. Este argumento se puede omitir para un ARCHIVO DLL independiente (XLL) que incluye una función [xlAutoRegister](xlautoregister-xlautoregister12.md) o **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** solo se admite en Excel 2007. 
  
Si se llama a **xlfRegister** con este argumento ausente, Excel llama a **xlAutoRegister** o **xlAutoRegister12**, si existe en la DLL especificada, que debe registrar correctamente la función proporcionando esta información.
  
_pxFunctionText_ (**xltypeStr**)
  
Nombre de la función tal como aparecerá en el Asistente para funciones. Este argumento es opcional; si se omite, la función no está disponible en el Asistente para funciones y solo se puede llamar mediante la función **CALL** mediante el identificador de registro de funciones de una hoja de macros XLM. Por lo tanto, para el uso normal de la hoja de cálculo, debe controlar este argumento según sea necesario. 
  
_pxArgumentText_ (**xltypeStr**)
  
Una cadena de texto opcional que describe los argumentos de la función. El usuario lo ve en el Asistente para funciones. Si se omite, Excel crea descripciones básicas a partir _de pxTypeText_.
  
_pxMacroType_ (**xltypeNum** o **xltypeInt**)
  
Argumento opcional que indica el tipo de punto de entrada XLL. El valor predeterminado, si se omite, es 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valor pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Se puede llamar desde una hoja de cálculo  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se puede llamar desde una hoja de macros  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se puede llamar desde una definición de nombre definida  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se puede llamar desde una expresión de formato condicional  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Enumerado en el Asistente para funciones para funciones de hoja de cálculo  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Enumerado en el Asistente para funciones para funciones de hoja de macros  <br/> |No  <br/> |Sí  <br/> |Sí  <br/> |
   
En la práctica, debe usar 1 para funciones de hoja de cálculo, 1 para funciones equivalentes de hoja de macros (registradas como tipo) a las que desea llamar desde la hoja de cálculo y 2 para **#** comandos. 
  
> [!NOTE]
> Los comandos XLL están ocultos y no se muestran en cuadros de diálogo para ejecutar macros, aunque sus nombres se pueden especificar en cualquier lugar en el que se requiera un nombre de comando válido. 
  
_pxCategory_ (**xltypeStr** o **xltypeNum**)
  
Argumento opcional que permite especificar a qué categoría debe pertenecer la nueva función o comando. El Asistente para funciones divide las funciones por tipo (categoría). Puede especificar un nombre de categoría o un número secuencial, donde el número es la posición en la que aparece la categoría en el Asistente para funciones. Para obtener más información, consulte la sección "Nombres de categoría". Si se omite, se asume la categoría Definido por el usuario.
  
_pxShortcutText_ (**xltypeStr**)
  
Una cadena que distingue mayúsculas de minúsculas de un carácter que especifica la clave de control asignada a este comando. Por ejemplo, "A" asigna este comando a CONTROL+MAYÚS+A. Este argumento es opcional y solo se usa para comandos.
  
_pxHelpTopic_ (**xltypeStr**)
  
Una referencia opcional al archivo de ayuda (.chm o .hlp) para mostrar cuando el usuario hace clic en el botón Ayuda (cuando se muestra la función personalizada). Puede estar en el formulario  `filepath!HelpContextID` o  `https://address/path_to_file_in_site!0` . Ambas partes antes y después del "!" son necesarias.  *HelpContextID* no debe contener comillas simples y se convertirá Excel un entero sin signo de 4 bytes de longitud, en forma decimal. Al usar el formulario de dirección URL, Excel solo abre el archivo de ayuda al que se hace referencia. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Una cadena opcional que describe la función personalizada cuando se selecciona en el Asistente para funciones.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Opcional. La primera de las cadenas que describen los argumentos personalizados de la función cuando se selecciona la función en el Asistente para funciones. En Excel 2003 y versiones anteriores, **xlfRegister** puede tomar, como máximo, 30 argumentos para que pueda proporcionar esta ayuda solo para los primeros 20 argumentos de función. A partir de Excel 2007, **xlfRegister** puede tomar hasta 255 argumentos para proporcionar esta ayuda para hasta 245 parámetros de función. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si el registro se realizó correctamente, esta función devuelve el identificador de registro de la función (**xltypeNum**), que se puede usar en llamadas a **xlUDF** y **xlfUnregister** en un DLL, o con **CALL** y **UNREGISTER** en una hoja de macros XLM. De lo contrario, devuelve un #VALUE! error. 
  
## <a name="remarks"></a>Comentarios

### <a name="data-types"></a>Tipos de datos

El  _argumento pxTypeText_ especifica el tipo de datos del valor devuelto y los tipos de datos de todos los argumentos de la función DLL o recurso de código. El primer carácter de  _pxTypeText_ especifica el tipo de datos del valor devuelto. Los caracteres restantes indican los tipos de datos de todos los argumentos. Por ejemplo, una función DLL que devuelve un número de punto flotante y toma un número entero y un número de punto flotante como argumentos requeriría "BIB" para el _argumento pxTypeText._ 
  
Los tipos de datos y estructuras usados por Excel para intercambiar datos con XLL se resumen en las dos tablas siguientes.
  
En la primera tabla se enumeran los tipos admitidos en todas las versiones de Excel.
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Booleano  <br/> |A  <br/> |L  <br/> |short [int] (0=false o 1=true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*   <br/> ||C, F  <br/> |Cadena de bytes en ASCII terminada en null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadena de bytes ASCII contada  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD de 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |Entero con signo de 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |Entero con signo de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Estructura de matriz con punto flotante  <br/> |
|Matriz  <br/> ||O  <br/> |Se pasan tres argumentos:<br/>- int corto sin signo \*<br/>- int corto sin signo \*<br/>- double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||R  <br/> |Referencias de rango, matrices y valores  <br/> |
   
En Excel 2007 se introdujeron los siguientes tipos de datos para admitir las cuadrículas más grandes y las cadenas Unicode largas.
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|short sin signo \*  <br/> ||C%, F%  <br/> |Cadena de caracteres anchos Unicode terminada en null  <br/> |
|short sin signo \*  <br/> ||D%, G%  <br/> |Cadena de caracteres anchos Unicode contada  <br/> |
|FP12  <br/> ||K%  <br/> |Estructura de matriz de punto flotante de cuadrícula más grande  <br/> |
|Matriz  <br/> ||O%  <br/> |Se pasan tres argumentos:<br/>- int \* / RW firmado \*<br/>- int \* / COL firmado \*<br/>- double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||U  <br/> |Referencias de rango, matrices y valores  <br/> |
   
A partir Excel 2010 se introdujeron los siguientes tipos de datos:
  
|**Tipo de datos**|**Paso por valor**|**Paso por referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |El identificador asincrónico se usa para realizar un seguimiento de una llamada de función asincrónica pendiente por parte de Excel y XLL.La existencia del tipo de parámetro en la cadena de tipo también designa la función como asincrónica. Para obtener más información acerca de las funciones asincrónicas, vea [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).  <br/> |
   
Los tipos de cadena **F**, **F%**, **G**, y **G%** se usan para los argumentos modificados en sitio.  
  
Al trabajar con los tipos de datos que se muestran en la tabla anterior, tenga en cuenta lo siguiente:
  
- Las declaraciones de lenguaje C suponen que el compilador usa dobles de 8 bytes, enteros cortos de 2 bytes y enteros de 4 bytes de forma predeterminada.
    
- Se llama a todas las funciones de dll y recursos de código mediante **la convención de __stdcall** de llamadas. 
    
- Cualquier función que devuelve un tipo de datos por referencia, es decir, que devuelve un puntero a algo, puede devolver de forma segura un puntero nulo. Excel interpreta un puntero nulo como un #NUM! error.
    
## <a name="additional-data-type-information"></a>Información de tipo de datos adicional

Esta sección contiene información detallada sobre los tipos de datos **E**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R** y **U,** y otra información sobre el _argumento pxTypeText._ 
  
### <a name="e-data-type"></a>Tipo de datos E

Excel espera que un DLL que use el tipo de datos E pase punteros a números de punto flotante en la pila. Esto puede provocar problemas con algunos idiomas (por ejemplo, Borland C++) que esperan que el número se pase a la pila del emulador de coprocesador. La solución alternativa es pasar un puntero al número de la pila de coprocesadores. En el ejemplo siguiente se muestra cómo devolver un doble de Borland C++.
  
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

Con los **tipos de** datos F , **F%**, **G** y **G%,** una función puede modificar un búfer de cadenas asignado por Excel. Si el código de tipo de valor devuelto es uno de estos tipos, Excel omite el valor devuelto por la función. En su lugar, Excel busca en la lista de argumentos de función el primer tipo de datos correspondiente (**F**, **F %**, **G** o **G %**) y, a continuación, toma el contenido actual del búfer de cadena asignado como valor devuelto. Todas las versiones de Excel asignan 256 bytes para las cadenas ASCII **F** y **G,** y a partir de Excel 2007 se asignan 65.536 bytes, suficientes para 32.768 caracteres Unicode, para las cadenas **Unicode F%** y **G%.** Recuerde que los búferes deben incluir un carácter de recuento (tipos **G** y **G%**) o un carácter de terminación nula (tipos **F** y **F%**), de modo que las longitudes máximas de cadena reales sean 255 y 32.767. Las cadenas Unicode y, por lo tanto, los argumentos **F%** y **G%** solo están disponibles a través de la API de C en Excel. 
  
### <a name="k-and-k-data-types"></a>Tipos de datos K y K%

Los **tipos de** datos K y **K%** usan punteros a las estructuras FP y FP12 de tamaño variable respectivamente. Estas estructuras se definen en XLLCALL.H. Las estructuras FP12 y, por lo tanto, los argumentos **K%** solo se admiten a partir Excel 2007. 
  
### <a name="o-and-o-data-types"></a>Tipos de datos O y O%

Los **tipos de** datos O y **O%** solo se pueden usar para argumentos, no para devolver valores, aunque los valores se pueden devolver al modificar un argumento de tipo **O** **o O%** en su lugar. Cada uno pasa tres elementos: un puntero al número de filas de una matriz, un puntero al número de columnas de una matriz y un puntero a una matriz bidimensional de números de punto flotante. 
  
Para modificar una matriz pasada por el tipo de datos O u O% en su lugar, puede usar ">O" o ">O%" como argumento _pxTypeText._ Para obtener más información acerca de cómo modificar una matriz, vea la sección "Modificar en su lugar: funciones declaradas como nulas" en este tema. 
  
El **tipo de** datos O se creó para la compatibilidad directa con las DLL de Fortran, que pasan argumentos por referencia. 
  
El **O%** se admite a partir Excel 2007 y se adapta al mayor número de filas que Excel admite. 
  
### <a name="p-and-q-data-types"></a>Tipos de datos P y Q

Cuando los argumentos de función DLL se registran como archivos **XLOPER** de tipo P o XLOPER12 de tipo **Q,** Excel convierte referencias de celda única a valores simples y referencias de varias celdas a matrices al preparar estos argumentos. En otras palabras, los tipos **P** y **Q** siempre llegarán a la función como uno de estos tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** o **xltypeNil**, pero no **xltypeRef** o **xltypeSRef** porque siempre se desreferencian. **Los argumentos XLOPER12** y, por lo tanto, **de tipo Q,** solo se admiten a partir Excel 2007. 
  
Si los **tipos xltypeMissing** o **xltypeNil** se usan para valores devueltos, se interpretan Excel como cero numérico. **xltypeMissing** se pasa cuando el autor de la llamada omite un argumento. **xltypeNil** se pasa cuando el autor de la llamada pasa una referencia a una celda vacía. Cuando un rango de celdas se convierte en **un xltypeMulti** que se pasará como tipo **P** o **Q**, las celdas en blanco dentro del rango se convierten en elementos de matriz **xltypeNil.** Los elementos que faltan en una matriz literal se pasan de forma similar a **los elementos xltypeNil.** 
  
### <a name="volatile-functions-and-recalculation"></a>Funciones volátiles y recálculo

En una hoja de cálculo, puede hacer que una función DLL o un recurso de código sea volátil, de modo que se recalcula cada vez que la hoja de cálculo vuelve a calcularse. Para ello, agregue un signo de exclamación (!) después del último código de argumento en el _argumento pxTypeText._ 
  
> [!NOTE]
> De forma predeterminada, las funciones que toman el tipo **R** XLOPER o **el** tipo U XLOPER12s y que están registradas como equivalentes de hoja de macros (tipo ; vea la sección siguiente) se controlan como **#** volátiles en Excel. 
  
### <a name="functions-declared-as-void"></a>Funciones declaradas como nulas

Hay dos casos que llaman para declarar una función como void de devolución. En ambos casos, la función devuelve su resultado por otros medios.
  
#### <a name="modifying-in-place"></a>Modificación en su lugar

Puede usar un solo dígito  _n_ para el código de tipo de devolución en  _pxTypeText_, donde  _n_ es un número del 1 al 9. Esto indica a Excel que tome el valor de la variable en la ubicación a la que apunta el argumento _n_th _pxTypeText_ como valor devuelto. Esto también se conoce como modificación en su lugar. El argumento _n_th debe ser un tipo de datos de paso por referencia (C, D, E, F, F%, G, G%, K, K%, L, M, N, O, O%, P, Q, R o U). La función DLL o el recurso de código también deben declararse con la palabra clave **void** en los idiomas C/C++ (o la palabra clave **procedure** en el lenguaje Pascal). 
  
Por ejemplo, una función DLL que toma una cadena terminada en null y dos punteros a enteros como argumentos puede modificar la cadena en su lugar. Usa "1FMM" como argumento  _pxTypeText_ y declara la función como void. 
  
Las versiones anteriores de Excel se usaban al principio de pxTypeText para indicar que la función se declaraba como nula y que el primer argumento se iba a modificar en su lugar; no había forma de modificar ningún argumento que no fuera el **\>** primero.  El **\>** valor es equivalente a _n_ = 1 en las versiones Excel actuales y este uso de en funciones sincrónicas solo es compatible con **\>** versiones anteriores. 
  
#### <a name="asynchronous-functions"></a>Funciones asincrónicas

Una función asincrónica, que se indica mediante un parámetro de tipo X en **pxTypeText**, no devuelve su resultado de la llamada de función inicial. En su lugar, debe declarar una función asincrónica como void y, posteriormente, el complemento devuelve el resultado a través de una devolución de llamada. La función asincrónica debe registrarse con el inicio **\>** de **pxTypeText**. En las funciones asincrónicas, indica que la función se declara como void, pero no indica que el **\>** primer argumento se modifique en su lugar. Para obtener más información acerca de las funciones asincrónicas, vea [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registro de funciones de hoja de cálculo como equivalentes de hoja de macros (control de celdas sin calcular)

Colocar un carácter después del último código de parámetro en pxTypeText proporciona a la función los mismos permisos de llamada que **#** las funciones de una hoja de macros.  Son las siguientes: 
  
- La función puede recuperar los valores de las celdas que aún no se han calculado en este ciclo de actualización.
    
- La función puede llamar a cualquiera de las funciones de información XLM (clase 2), por ejemplo, **xlfGetCell**.
    
- Si el signo de número (#) no está presente: la evaluación de una celda sin calcular da como resultado un error **xlretUncalced** y se vuelve a llamar a la función actual una vez calculada la celda; llamar a cualquier función de información XLM que no sea **xlfCaller** da como resultado un error **xlretInvXlfn.** 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrar funciones de hoja de cálculo como seguras para subprocesos

A partir de Excel 2007, Excel puede realizar una actualización de libro multiproceso. Esto significa que puede asignar diferentes instancias de una función segura para subprocesos a subprocesos simultáneos para su reevaluación. A partir Excel 2007, la mayoría de las funciones de hoja de cálculo integradas son seguras para subprocesos. A partir Excel 2007, Excel también permite que los XLL registren funciones de hoja de cálculo como seguras para subprocesos. Para ello, incluya un carácter después del último código **$** de parámetro en  _pxTypeText_. 
  
> [!NOTE]
> Solo las funciones de hoja de cálculo se pueden declarar como seguras para subprocesos. Excel considera que una función equivalente de hoja de macros es segura para subprocesos, por lo que no puede anexar ambos caracteres al **#** **$** argumento _pxTypeText._ 
  
Si ha registrado una función como segura para subprocesos, debe asegurarse de que se comporta de forma segura para subprocesos, aunque Excel rechaza las llamadas que no son seguras para subprocesos a través de la API de C. Por ejemplo, si una función segura para subprocesos intenta llamar a **xlfGetCell**, la llamada falla con el error **xlretNotThreadSafe.** 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrar funciones de hoja de cálculo como seguras para clústeres

A partir Excel 2010, Excel puede descargar llamadas de función a un proveedor de clúster de cálculo designado. Para obtener más información, vea [Cluster Caja fuerte Functions](cluster-safe-functions.md). Las funciones de hoja de cálculo XLL registradas como seguras para clústeres participan en la descarga si hay un clúster disponible. Las funciones seguras para clústeres se registran al incluir el carácter después del **&amp;** último código de parámetro en el argumento _pxTypeText._ 
  
Si ha registrado una función como segura para clústeres, debe asegurarse de que se comporta de forma segura para clústeres. Para obtener más información, vea [Cluster Caja fuerte Functions](cluster-safe-functions.md).
  
> [!NOTE]
> Solo las funciones de hoja de cálculo se pueden declarar como seguras para clústeres. Excel considera que una función equivalente de hoja de macros es segura para clústeres, por lo que no puede anexar ambos caracteres al **#** **&amp;** argumento _pxTypeText._ Las funciones de hoja de cálculo se pueden declarar como seguras para clústeres y seguras para subprocesos. En este caso, Excel estas funciones participarán en el recálculo multiproceso cuando se deshabilita la descarga del clúster. 
  
### <a name="category-names"></a>Nombres de categoría

Use las siguientes directrices para determinar en qué categoría se deben colocar las funciones XLL.
  
- Si la función hace algo que podría hacer el usuario como parte de la interfaz de usuario del complemento, debe colocar la función en la **categoría** Comandos. 
    
- Si la función devuelve información sobre el estado del complemento o cualquier otra información útil, debe colocar la función en la **categoría** Información. 
    
- Un complemento nunca debe agregar funciones o comandos a la **categoría Definido por** el usuario. Esta categoría es para el uso exclusivo de los usuarios finales. 
    
La categoría se especifica mediante el  _parámetro pxCategory_ para **xlfRegister**. Puede ser un número o texto que corresponda a una de las categorías estándar codificadas de forma inefi ó el texto de una nueva categoría especificada por la DLL. Si el texto dado aún no existe, Excel una nueva categoría con ese nombre.
  
En la tabla siguiente se enumeran las categorías estándar que están visibles al ver el cuadro de diálogo **Función** pegar desde dentro de una hoja de cálculo. 
  
|**Number**|**Texto**|
|:-----|:-----|
|1  <br/> |Financiera  <br/> |
|2  <br/> |Fecha &amp; y hora  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4   <br/> |Texto  <br/> |
|5   <br/> |Lógicas  <br/> |
|6   <br/> |Lookup &amp; Reference  <br/> |
|7   <br/> |Database  <br/> |
|8   <br/> |Estadísticas  <br/> |
|9   <br/> |Información  <br/> |
|14   <br/> |Definidas por el usuario  <br/> |
||Ingeniería (a partir de Excel 2007)  <br/> |
||Cubo (a partir de Excel 2007)  <br/> |
   
Además, estas categorías también son visibles al ver el cuadro de diálogo **Función** pegar desde dentro de una hoja de macros. 
  
|**Number**|**Texto**|
|:-----|:-----|
|10  <br/> |Comandos  <br/> |
|11  <br/> |DDE/Externas  <br/> |
|12   <br/> |Personalización  <br/> |
|13  <br/> |Control de macros  <br/> |
   
### <a name="example"></a>Ejemplo

Vea el código de la **función xlAutoOpen** en  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Vea también

- [REGISTER.ID](xlfregisterid.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

