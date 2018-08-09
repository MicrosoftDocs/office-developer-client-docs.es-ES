---
title: Tipos de datos de Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- tipos de datos de registro [excel 2007], tipos de datos, las cadenas [Excel 2007], números [Excel 2007], estructuras de datos [Excel 2007], [Excel 2007] los tipos de datos de Excel
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815533"
---
# <a name="data-types-used-by-excel"></a>Tipos de datos de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel intercambia varios tipos de ANSI C o C++ y también algunas estructuras de datos específicas de Excel. Se mencionan aquí para proporcionar un contexto de otras secciones, y se explican en detalle en el tema [xlfRegister (formulario 1)](xlfregister-form-1.md) . 
  
## <a name="ansi-cc-types"></a>Tipos de ANSI C o C++

### <a name="numbers"></a>Números

Todas las versiones de Excel:
  
- doble de 8 bytes
    
- [con signo] short [int] &ndash; usado para los valores **booleanos** y también enteros 
    
- short sin signo [int]
    
- [long con signo] int
    
### <a name="strings"></a>Strings

Todas las versiones de Excel:
  
- char [con signo] \* &ndash; cadenas de bytes terminada en null de hasta 255 caracteres
    
- unsigned char \* &ndash; cadenas de bytes de longitud contada de hasta 255 caracteres
    
Iniciar en Excel 2007:
  
- short sin signo \* &ndash; cadenas Unicode de hasta 32.767 caracteres, que pueden ser terminada en null o longitud contada
    
Todos los números de hoja de cálculo en Excel se almacenan como valores de modo que no es necesario (y de hecho presenta una sobrecarga de conversión pequeñas) para declarar funciones como el intercambio de tipos de enteros con Excel.
  
Cuando se utilizan tipos de entero, Excel comprueba que las entradas son dentro de los límites del tipo, y producirá un error con **#NUM!** Si está fuera de éstos. La excepción se produce cuando se está registrando una función para tomar un argumento de **tipo Boolean** , implementado con int. corto En este caso, cualquier entrada distinto de cero se convierte en 1 y cero se pasa directamente a través de. 
  
## <a name="excel-specific-data-structures"></a>Estructuras de datos específicas de Excel

Todas las versiones de Excel:
  
- **FP** &ndash; una estructura de matriz bidimensional de punto flotante que admite 65.356 filas por el número máximo de columnas compatibles con la versión determinada de Excel. 
    
- **XLOPER** &ndash; una estructura de datos de varios tipos que puede representar todos los tipos de datos de hoja de cálculo (incluidos los errores), números enteros, referencias de rango, tipos de control de flujo de hoja de macro XLM y un tipo de datos binarios de almacenamiento interno. 
    
   > [!NOTE]
   > Las cadenas se representan como cadenas de longitud contada byte de hasta 255 caracteres de longitud. 
  
Iniciar en Excel 2007:
  
- **FP12** &ndash; una estructura de matriz bidimensional de punto flotante que admite todas las filas y columnas a partir de Excel 2007. 
    
- **XLOPER12** &ndash; una estructura de datos de varios tipos que puede representar todos los tipos de datos de hoja de cálculo (incluidos los errores), números enteros, referencias de rango, tipos de control de flujo de hoja de macro XLM y un tipo de datos binarios de almacenamiento interno. 
    
   > [!NOTE]
   > Las cadenas se representan como cadenas Unicode de longitud contada de hasta 32.767 caracteres de largos. 
  
## <a name="registration-data-type-codes"></a>Códigos de tipo de datos de registro

Funciones XLL se registran con el de función API C **xlfRegister**, que toma como argumento tercer una cadena de letras que codifican los tipos de devolución y argumento. Esta cadena también contiene la información que indica a Excel si la función es volátil, es segura para los subprocesos (comenzando en Excel 2007), es el equivalente de hoja de macros, y si se devuelve su resultado mediante la modificación de un argumento en su lugar.
  
En la siguiente tabla se reproducen y tratan con más detalle en el tema [xlfRegister (formulario 1)](xlfregister-form-1.md) . Se reproduce aquí con el fin de proporcionar un contexto para el resto de esta sección. Por ejemplo, se podría describir una función que toma una cadena de Unicode de longitud contada (comenzando en Excel 2007) que toma un tipo de argumento de C %. 
  
|Tipo de datos|Pasar por valor|Pase mediante referencia (puntero)|Comentarios|
|:-----|:-----|:-----|:-----|
|Booleano  <br/> |A  <br/> |L  <br/> |short (0 = false o 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |Cadena de bytes ASCII terminada en null  <br/> |
|char sin signo\*  <br/> ||D., G  <br/> |Longitud-cadena de bytes ASCII contada  <br/> |
|short sin signo \* (comenzando en Excel 2007)  <br/> ||C %, F %  <br/> |Cadena de caracteres anchos de Unicode terminada en null  <br/> |
|short sin signo \* (comenzando en Excel 2007)  <br/> ||% D, % G  <br/> |Cadena de caracteres anchos de Unicode de longitud contada  <br/> |
|short sin signo [int]  <br/> |H  <br/> ||WORD  <br/> |
|[con signo] short [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[long con signo] int  <br/> |J  <br/> |N  <br/> |32-bit  <br/> |
|Matriz  <br/> ||O  <br/> | Que se pasa como tres argumentos por referencia:  <br/>1. short int \*filas  <br/>2. short int \*columnas  <br/>3. double \*matriz  <br/> |
|Matriz  <br/> (comenzando en Excel 2007)  <br/> ||% O  <br/> | Que se pasa como tres argumentos por referencia:  <br/>1. int \*filas  <br/>2. int \*columnas  <br/>3. double \*matriz  <br/> |
|FP  <br/> ||K  <br/> |Estructura de matriz de coma flotante  <br/> |
|FP12  <br/> (comenzando en Excel 2007)  <br/> ||% K  <br/> |Estructura de matriz de coma flotante de cuadrícula grande  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrices y valores de la hoja de cálculo de tipo de variable  <br/> |
|||L  <br/> |Valores, matrices y referencias de rango  <br/> |
|XLOPER12  <br/> (comenzando en Excel 2007)  <br/> ||Q  <br/> |Matrices y valores de la hoja de cálculo de tipo de variable  <br/> |
|||U  <br/> |Valores, matrices y referencias de rango  <br/> |
   
Los tipos **C %**, **F %**, **D %**, **G %**, **K %**, **O %**, **Q**y **U** eran todos los nuevos en Microsoft Office Excel 2007 y no son compatibles con versiones anteriores. Los tipos de cadena **F**, **F %**, **G**y **G %** se usan para los argumentos que son modificado en contexto. Cuando **XLOPER** o **XLOPER12** argumentos se registran como tipo **P** o **Q** respectivamente, Excel convierte las referencias de celda de un solo a valores simples y referencias de varias celdas a matrices cuando los prepara. 
  
Tipos **P** y **Q** siempre llegan a la función como uno de los siguientes tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**o **xltypeNil**, pero no **xltypeRef** o **xltypeSRef** debido a que estos siempre se eliminan las referencias. 
  
Tipo **O**, que es en realidad tres argumentos en la pila, se introdujo para la compatibilidad con archivos DLL Fortran donde los argumentos se pasan por referencia. No se puede utilizar para devolver un valor, excepto por el argumento como un valor devuelto de modificar en lugar de declarar y colocar los resultados en los valores que se hace referencia. Escriba **% O** extiende de tipo **O** en Excel 2007 para que puede obtener acceso a las matrices que cubren áreas mayores que la cuadrícula de Office Excel 2003. 
  
## <a name="see-also"></a>Vea también

- [xlfRegister (Formulario 1)](xlfregister-form-1.md)
- [Conceptos de programación de Excel](excel-programming-concepts.md)
- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

