---
title: xlfRegister (Formulario 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385084"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formulario 1)

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel. Esto equivale a llamar a **registrar** desde una hoja de macros XLM de Excel. 
  
puede llamar a **xlfRegister** de dos formas: 
  
- xlfRegister (formulario 1): registra un solo comando o una función.
    
- [xlfRegister (formulario 2)](xlfregister-form-2.md): cargas y se activa un XLL.
    
Llama a en el formulario 1, esta función permite que un comando o función DLL esté disponible para Excel, el recuento de uso establece en 1 y devuelve su identificador de registro, que se puede utilizar para llamar a la función más adelante mediante la [xlUDF](xludf.md) o la función **xlfCall** . El identificador de registro también se usa para anular el registro de la función mediante [xlfUnregister (formulario 1)](xlfunregister-form-1.md). Si la función se ha registrado, volver a llamar a **xlfRegister** incrementa el recuento de uso. 
  
Esta forma de la función también define un nombre oculto que es el argumento de texto de la función, _pxFunctionText_, y que se evalúa en el identificador de registro de la función o el comando. Cuando anula el registro de la función, eliminar este nombre con el [xlfSetName](xlfsetname.md). Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
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

## <a name="parameters"></a>Parámetros

_pxModuleText_ (**xltypeStr**)
  
El nombre de la DLL que contiene la función. Esto puede obtenerse mediante una llamada a la función sólo XLL [xlGetName](xlgetname.md) si la función registrada es también dentro de la DLL que se está ejecuta actualmente. 
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si una cadena, el nombre de la función para llamar a tal como se aparece en el código del archivo DLL. Si un número, el ordinal exportar el número de la función que se llama. Para mayor claridad, utilice siempre la forma de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de argumentos de la función y el tipo del valor devuelto de la función. Si desea más información, vea la sección Comentarios. Este argumento puede omitirse para un archivo DLL independiente (XLL) que incluye una [función xlAutoRegister](xlautoregister-xlautoregister12.md) o **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** sólo se admite en Excel 2007. 
  
Si se llama a **xlfRegister** con este argumento falta, Excel llama a **xlAutoRegister** o **xlAutoRegister12**, si bien existe en el archivo DLL especificado, que debe correctamente, a continuación, registrar la función al proporcionar esta información.
  
_pxFunctionText_ (**xltypeStr**)
  
El nombre de la función tal y como aparecerá en el Asistente para la función. Este argumento es opcional; Si se omite, la función no está disponible en el Asistente para la función y sólo se puede llamar mediante la función **de llamadas** con el identificador de registro de las funciones de una hoja de macros XLM. Por lo tanto, para el uso normal de la hoja de cálculo, se debe controlar este argumento según sea necesario. 
  
_pxArgumentText_ (**xltypeStr**)
  
Una cadena de texto opcional que describe los argumentos a la función. El usuario ve esto en el Asistente para la función. Si se omite, Excel construye descripciones básicas de _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** o **xltypeInt**)
  
Elija un argumento opcional que indica el tipo de entrada XLL. El valor predeterminado, si se omite, es 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valor de pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Se pueden llamar desde una hoja de cálculo  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se pueden llamar desde una hoja de macros  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se pueden llamar desde una definición de nombre definido  <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|Se pueden llamar desde una expresión de formato condicional  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Que aparecen en el Asistente para funciones para las funciones de hoja de cálculo  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Que aparecen en el Asistente para funciones para las funciones de hoja de macro  <br/> |No  <br/> |Sí  <br/> |Sí  <br/> |
   
En la práctica, debe usar 1 para las funciones de hoja de cálculo, 1 para funciones de hoja de macros de equivalente (registrada como tipo **#**) que desea llamar desde la hoja de cálculo y 2 para los comandos. 
  
> [!NOTE]
> Comandos XLL están ocultos y no se muestran en cuadros de diálogo para la ejecución de macros, aunque sus nombres se pueden escribir en cualquier lugar se requiere un nombre de comando válido. 
  
_pxCategory_ (**xltypeStr** o **xltypeNum**)
  
Un argumento opcional que permite especificar qué categoría de la nueva función o el comando debe pertenecer a. El Asistente para la función divide funciones por tipo (categoría). Puede especificar un nombre de categoría o un número secuencial, donde el número es la posición en la que la categoría aparece en el Asistente para la función. Para obtener más información, vea la sección "Nombres de categoría". Si se omite, se supone la categoría definida por el usuario.
  
_pxShortcutText_ (**xltypeStr**)
  
Una cadena de un carácter, entre mayúsculas y minúsculas que especifica la clave de control asignada a este comando. Por ejemplo, "A" asigna este comando al CONTROL + MAYÚS + A. Este argumento es opcional y se usa para comandos sólo.
  
_pxHelpTopic_ (**xltypeStr**)
  
Una referencia opcional para el archivo de ayuda (.chm o .hlp) que se mostrará cuando el usuario hace clic en el botón de ayuda (cuando se muestra la función personalizada). Puede ser en el formulario `filepath!HelpContextID` o `https://address/path_to_file_in_site!0`. Ambos elementos antes y después de la "!" son necesarios.  *HelpContextID* no debe contener comillas simples y Excel convertirá en un entero sin signo de 4 bytes de longitud, en formato decimal. Cuando se usa el formulario de dirección URL, abre Excel sólo el archivo de ayuda que se hace referencia. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Una cadena opcional que describe la función personalizada cuando está seleccionado en el Asistente para la función.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Opcional. La primera de las cadenas que se describen los argumentos de la función personalizados cuando se selecciona la función en el Asistente para la función. En Excel 2003 y versiones anteriores, **xlfRegister** puede tomar, como máximo, 30 argumentos para que puedan proporcionar esta ayuda para el primer 20 de sólo los argumentos de función. Iniciar en Excel 2007, **xlfRegister** puede tardar hasta 255 argumentos para que puedan proporcionar esta ayuda hasta 245 para parámetros de función. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si el registro se realizó correctamente, esta función devuelve el identificador de registro de la función (**xltypeNum**), que se puede utilizar en las llamadas a **xlUDF** y **xlfUnregister** en un archivo DLL o con **llamadas** y **eliminación del registro** en una hoja de macros XLM. ¡De lo contrario, devuelve #VALUE! error. 
  
## <a name="remarks"></a>Comentarios

### <a name="data-types"></a>Tipos de datos

El argumento _pxTypeText_ especifica el tipo de datos del valor devuelto y los tipos de datos de todos los argumentos de la función de DLL para el recurso de código. El primer carácter de _pxTypeText_ especifica el tipo de datos del valor devuelto. El resto de los caracteres indica los tipos de datos de todos los argumentos. Por ejemplo, una función DLL que devuelve un número de punto flotante y toma un entero y un número de punto flotante como argumentos requeriría "BIBLIOGRÁFICA" para el argumento _pxTypeText_ . 
  
En las dos tablas siguientes se resumen los tipos de datos y estructuras usadas por Excel para intercambiar datos con los XLL.
  
La primera tabla enumera los tipos admitidos en todas las versiones de Excel.
  
|**Tipo de datos**|**Pasar por valor**|**Pase mediante referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Booleano  <br/> |A  <br/> |L  <br/> |short [int] (0 = false o 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |Cadena de bytes ASCII terminada en null  <br/> |
|char sin signo\*  <br/> ||D., G  <br/> |Cadena de bytes ASCII contada  <br/> |
|short sin signo [int]  <br/> |H  <br/> ||PALABRA de 16 bits  <br/> |
|[con signo] short [int]  <br/> |I  <br/> |M  <br/> |entero con signo de 16 bits  <br/> |
|[long con signo] int  <br/> |J  <br/> |N  <br/> |entero con signo de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Estructura de matriz de coma flotante  <br/> |
|Matriz  <br/> ||O  <br/> |Se pasan tres argumentos:<br/>-int corto sin firmar\*<br/>-int corto sin firmar\*<br/>-double]  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrices y valores de la hoja de cálculo de tipo de variable  <br/> |
|||L  <br/> |Valores, matrices y referencias de rango  <br/> |
   
En Excel 2007 que se introdujeron los siguientes tipos de datos admitir las cuadrículas más grandes y Unicode largo cadenas.
  
|**Tipo de datos**|**Pasar por valor**|**Pase mediante referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|short sin signo\*  <br/> ||C %, F %  <br/> |Cadena de caracteres anchos de Unicode terminada en null  <br/> |
|short sin signo\*  <br/> ||% D, % G  <br/> |Cadena de caracteres anchos Unicode contada  <br/> |
|FP12  <br/> ||% K  <br/> |Estructura de matriz de coma flotante de cuadrícula más grande  <br/> |
|Matriz  <br/> ||% O  <br/> |Se pasan tres argumentos:<br/>-firmado int \* / RW\*<br/>-firmado int \* / COL\*<br/>-double]  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Matrices y valores de la hoja de cálculo de tipo de variable  <br/> |
|||U  <br/> |Valores, matrices y referencias de rango  <br/> |
   
Iniciar en Excel 2010 los siguientes datos se introdujeron tipos:
  
|**Tipo de datos**|**Pasar por valor**|**Pase mediante referencia (puntero)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |El controlador asincrónico se usa para realizar un seguimiento de una llamada de función asincrónicas pendientes en Excel y el XLL. La existencia del tipo de parámetro en la cadena de tipo también designa la función como asincrónica. Para obtener más información acerca de las funciones asincrónicas, vea [Funciones de Asynchronous User-Defined](asynchronous-user-defined-functions.md).  <br/> |
   
Los tipos de cadena **F**, **F %**, **G**y **G %** se usan para los argumentos que son modificado en contexto. 
  
Cuando se trabaja con los tipos de datos que se muestran en la tabla anterior, tenga en cuenta de las siguientes opciones:
  
- Las declaraciones de lenguaje C se suponen que el compilador usa Double de 8 bytes, 2 bytes enteros cortos y enteros largos de 4 bytes de forma predeterminada.
    
- Todas las funciones en archivos DLL y recursos de código se llama utilizando la convención de llamada **__stdcall** . 
    
- Cualquier función que devuelve un tipo de datos por referencia, es decir, que devuelve un puntero a algo, puede devolver un puntero null de manera segura. ¡Excel interpreta un puntero null como un #NUM! error.
    
## <a name="additional-data-type-information"></a>Información de tipo de datos adicionales

Esta sección contiene información detallada sobre la **E**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R**y los tipos de datos **U** y otra información acerca de la pxTypeText _ _argumento. 
  
### <a name="e-data-type"></a>Tipo de datos E

Excel espera que un archivo DLL mediante el tipo de datos E para pasar punteros a números de punto flotante en la pila. Esto puede causar problemas con algunos idiomas (por ejemplo, Borland C++) que se espera que el número que se pasan en la pila de emulador coprocesador. La solución consiste en pasar un puntero para el número de la pila de coprocesador. En el ejemplo siguiente se muestra cómo devolver un valor double de Borland C++.
  
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

### <a name="f-f-g-and-g-data-types"></a>F, F %, G y G % los tipos de datos

Con la **F**, **F %**, **G**y **G %** los tipos de datos, una función puede modificar un búfer de cadena que se asigna por Excel. Si el código de tipo de valor devuelto es uno de estos tipos, Excel pasa por alto el valor devuelto por la función. En su lugar, Excel busca en la lista de argumentos de función el primer tipo de datos correspondiente (**F**, **F %**, **G**o **G %**) y, a continuación, toma el contenido actual del búfer de cadena asignada como el valor devuelto. Todas las versiones de Excel asignan 256 bytes para **F** y cadenas de ASCII **G** y, a partir de Excel 2007 65.536 bytes que se asignan, suficiente para 32.768 caracteres Unicode, **F %** y de cadenas de Unicode de **% G** . Recuerde que deben incluir los búferes de un carácter de recuento (tipos **G** y **G %**) o un carácter de terminación null (tipos de **F** y **F %**), por lo que la longitud máxima de la cadena real es 255 y 32.767. Cadenas Unicode y, por lo tanto, tipo argumentos **F** y **G %** , sólo están disponibles mediante la API C en Excel. 
  
### <a name="k-and-k-data-types"></a>K y tipos de datos de % K

Los tipos de datos **K** y **% K** usan punteros a las estructuras de tamaño variable FP y FP12 respectivamente. Estas estructuras se definen en XLLCALL. H. Estructuras de FP12 y, por lo tanto, los argumentos de tipo **K %** , solo se admiten a partir de Excel 2007. 
  
### <a name="o-and-o-data-types"></a>O y tipos de datos O %

Los tipos de datos **O** y **O %** sólo se puede usar para argumentos, no devuelven valores, aunque se pueden devolver valores mi modificación de un argumento de tipo **O** o **% O** en contexto. Cada uno de ellos pasa tres elementos: un puntero para el número de filas en una matriz, un puntero para el número de columnas en una matriz y un puntero a una matriz bidimensional de números de punto flotante. 
  
Para modificar una matriz pasada por el O u O escriba % datos en su lugar, puede utilizar "> O" o "> O %" como el argumento _pxTypeText_ . Para obtener más información acerca de cómo modificar una matriz, vea la sección "Modificar in situ: funciones declaradas como Void" en este tema. 
  
El tipo de datos **O** se creó para compatibilidad directa con los archivos DLL Fortran, que pasan argumentos por referencia. 
  
El **% O** se admite a partir de Excel 2007 y admite al número mayor de filas que es compatible con Excel. 
  
### <a name="p-and-q-data-types"></a>Tipos de datos P y Q

Cuando los argumentos de función DLL se registran como teniendo tipo **P** XLOPER o escriba **Q** XLOPER12s, Excel convierte las referencias de celda de un solo a valores simples y referencias de varias celdas a matrices al preparar estos argumentos. En otras palabras, tipos **P** y **Q** siempre llegarán en su función como uno de estos tipos: xltypeNil **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**o ** **, pero no **xltypeRef** o **xltypeSRef** debido a que estos siempre se eliminan las referencias. **XLOPER12**s y, por lo tanto, los argumentos de tipo **Q** , solo se admiten a partir de Excel 2007. 
  
Si se utiliza tipos **xltypeMissing** o **xltypeNil** para los valores devueltos, se interpretan por Excel como cero numérico. Cuando el autor de la llamada omite un argumento, se pasa **xltypeMissing** . **xltypeNil** se pasa cuando el autor de la llamada pasa una referencia a una celda vacía. Cuando un rango de celdas se convierte en un **xltypeMulti** que se pasan como tipo **P** o **Q**, las celdas en blanco dentro del intervalo se convierten en elementos de la matriz **xltypeNil** . Elementos que faltan en una matriz de literales de forma similar se pasan como elementos de **xltypeNil** . 
  
### <a name="volatile-functions-and-recalculation"></a>Funciones volátiles y recálculo

En una hoja de cálculo, puede realizar una función DLL para el recurso de código volátil, por lo que vuelve a calcular cada vez que vuelve a calcular la hoja de cálculo. Para ello, agregue un signo de exclamación (!) después del último código de argumento en el argumento _pxTypeText_ . 
  
> [!NOTE]
> De forma predeterminada, las funciones que toman tipo **R** XLOPER o escriba **U** XLOPER12s y que se registran como macro hoja equivalentes (tipo **#**; vea la sección siguiente) se tratan como volátil en Excel. 
  
### <a name="functions-declared-as-void"></a>Funciones declaradas como void

Hay dos casos que llamar para declarar una función devolver void. En ambos casos, la función devuelve su resultado por otro medio.
  
#### <a name="modifying-in-place"></a>Modificar in situ

Puede usar un único dígito _n_ para el código de tipo de valor devuelto en _pxTypeText_, donde _n_ es un número del 1 al 9. Esto indica a Excel que tomará el valor de la variable en la ubicación indicada por el argumento de _n_th en _pxTypeText_ como el valor devuelto. Esto se conoce también como modificar in situ. El argumento _n_th debe ser de tipo de datos de pase por referencia (C, D, E, F, F %, G, G %, K, K %, L, M, N, O, O %, P, Q, R o U). La función de DLL para el recurso de código también se debe declarar con la palabra clave **void** en los lenguajes C o C++ (o la palabra clave **procedure** en lenguaje Pascal). 
  
Por ejemplo, una función de DLL que toma una cadena terminada en null y dos punteros a enteros como argumentos pueden modificar la cadena in situ. Utilice "1FMM" como el argumento de _pxTypeText_ y declare la función como void. 
  
Las versiones anteriores de Excel que usa **\>** al principio de _pxTypeText_ para indicar que la función se declaró como void y que el primer argumento era que desea modificar en contexto: se ha producido ninguna forma de modificar cualquier argumento que no sea la primera. El **\>** es equivalente a _n_ = 1 en las versiones actuales de Excel y este uso de **\>** en funciones sincrónicas se admite para la compatibilidad con versiones anteriores. 
  
#### <a name="asynchronous-functions"></a>Funciones asincrónicas

Una función asincrónica, indicada mediante el uso de un parámetro de tipo X en **pxTypeText**, no devuelve su resultado de la llamada de función inicial. En su lugar, debe declarar una función asincrónica como void y más adelante el complemento devuelve el resultado a través de una devolución de llamada. La función asincrónica debe estar registrada mediante el uso de **\>** al principio de **pxTypeText**. En funciones asincrónicas, **\>** indica que la función se declara como void, pero no indica que se modifica el primer argumento en su lugar. Para obtener más información acerca de las funciones asincrónicas, vea [Funciones de Asynchronous User-Defined](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrar las funciones de hoja de cálculo como equivalentes de hojas de macro (controlar las celdas sin calcular)

Colocar un **#** después de que el último parámetro el código en _pxTypeText_ proporciona la función los mismos permisos llamados como funciones en una hoja de macros de caracteres. Estos son los siguientes: 
  
- La función puede recuperar los valores de las celdas que aún no se ha calculado en este ciclo de actualización.
    
- La función puede llamar a cualquiera de las funciones de información (clase 2) XLM, por ejemplo, **xlfGetCell**.
    
- Si no está presente el signo de número (#): evaluar el resultado de un error **xlretUncalced** y la función actual en una celda no calculada se vuelve a llamar una vez que se ha calculado la celda; llamar a cualquier función de información XLM que no sean **xlfCaller** da como resultado un error **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrar las funciones de hoja de cálculo como seguros para subprocesos

Iniciar en Excel 2007, Excel puede realizar cálculos de libro multiproceso. Esto significa que pueden asignar distintas instancias de una función de seguros para subprocesos a subprocesos simultáneos para reevaluación. Iniciar en Excel 2007, la mayoría de las funciones de hoja de cálculo integradas son seguros para subprocesos. Iniciar en Excel 2007, Excel también permite XLL registrar las funciones de hoja de cálculo como seguros para subprocesos. Para ello, incluya un **$** carácter después del último código de parámetro en _pxTypeText_. 
  
> [!NOTE]
> Funciones de hoja de cálculo sólo pueden declararse como seguros para subprocesos. Excel no tiene en cuenta una función equivalente de hoja macro para ser seguros para subprocesos, por lo que no se puede anexar ambos **#** y **$** caracteres para el argumento _pxTypeText_ . 
  
Si se ha registrado una función como seguros para subprocesos, debe asegurarse de que se comporta de manera segura para subprocesos, aunque Excel rechaza todas las llamadas a través de la API C no seguras subproceso. Por ejemplo, si una función de subprocesos intenta llamar a **xlfGetCell**, la llamada se produce un error con el error **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrar las funciones de hoja de cálculo como seguras de clúster

Iniciar en Excel 2010, Excel puede descargar las llamadas de función a un proveedor de clúster compute designada. Para obtener más información, vea [Funciones seguras de clúster](cluster-safe-functions.md). Todas las funciones de hoja de cálculo XLL registradas como segura para el clúster de participar en la descarga de si un clúster está disponible. Funciones seguras de clúster se registran mediante la inclusión de la **&amp;** carácter después del último código de parámetro en el argumento _pxTypeText_ . 
  
Si se ha registrado una función como seguras de clúster, debe asegurarse de que se comporta de forma segura para el clúster. Para obtener más información, vea [Funciones seguras de clúster](cluster-safe-functions.md).
  
> [!NOTE]
> Funciones de hoja de cálculo sólo pueden declararse como seguras de clúster. Excel no tiene en cuenta una función equivalente de hoja macro a ser seguras de clúster, por lo que no se puede anexar ambos **#** y **&amp;** caracteres para el argumento _pxTypeText_ . Funciones de hoja de cálculo se pueden declarar como seguras de clúster y seguros para subprocesos. En este caso, Excel le permitirá estas funciones a participar en el nuevo cálculo multiproceso cuando se deshabilita la descarga de clúster. 
  
### <a name="category-names"></a>Nombres de categorías

Use las siguientes instrucciones para determinar qué categoría para poner su XLL funciona en.
  
- Si la función hace algo que podría llevarse a cabo por el usuario como parte de la interfaz de usuario, debe colocar la función en la categoría de **comandos** . 
    
- Si la función devuelve información sobre el estado del complemento o cualquier otra información útil, debe colocar la función en la categoría de **información** . 
    
- Un complemento nunca debe agregar funciones o comandos a la categoría **Definida por el usuario** . Esta categoría es para uso exclusivo de los usuarios finales. 
    
La categoría se especifica mediante el parámetro _pxCategory_ para **xlfRegister**. Esto puede ser un número o texto que corresponde a una de las categorías estándares codificado de forma rígida o el texto de una nueva categoría especificada por el archivo DLL. Si el texto que aparece no existe ya, Excel crea una nueva categoría con ese nombre.
  
En la siguiente tabla se enumera las categorías estándares que son visibles al ver el cuadro de diálogo **Pegar función** desde dentro de una hoja de cálculo. 
  
|**Número**|**Text**|
|:-----|:-----|
|1  <br/> |Financiero  <br/> |
|2  <br/> |Fecha &amp; tiempo  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4  <br/> |Texto  <br/> |
|5  <br/> |Lógicos  <br/> |
|6  <br/> |Búsqueda &amp; referencia  <br/> |
|7  <br/> |Base de datos  <br/> |
|8  <br/> |Estadísticas  <br/> |
|9  <br/> |Información  <br/> |
|14  <br/> |Definidas por el usuario  <br/> |
||Ingeniería (comenzando en Excel 2007)  <br/> |
||Cubo (comenzando en Excel 2007)  <br/> |
   
Además, estas categorías también son visibles cuando se visualizan en el cuadro de diálogo **Pegar función** desde dentro de una hoja de macros. 
  
|**Número**|**Text**|
|:-----|:-----|
|10  <br/> |Comandos  <br/> |
|11  <br/> |DDE/Externas  <br/> |
|12  <br/> |Personalización  <br/> |
|13  <br/> |Control de macros  <br/> |
   
### <a name="example"></a>Ejemplo

Vea el código para la función **xlAutoOpen** en `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Vea también

- [ID.](xlfregisterid.md)
- [ANULAR EL REGISTRO](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

