---
title: Tipos de datos de Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- tipos de datos de registro [excel 2007], tipos de datos de Excel, cadenas [Excel 2007], números [Excel 2007], estructuras de datos [Excel 2007], tipos de datos [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c546fc80b212301689744d3279a59733d9cc5524
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710611"
---
# <a name="data-types-used-by-excel"></a>Tipos de datos de Excel

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel intercambia varios tipos en ANSI C o C++ y también algunas estructuras de datos específicas de Excel. Se mencionan aquí para proporcionar un contexto para otras secciones y se describen en detalle en el tema [xlfRegister (Formulario 1)](xlfregister-form-1.md). 
  
## <a name="ansi-cc-types"></a>Tipos en ANSI C o C++

### <a name="numbers"></a>Números

Todas las versiones de Excel:
  
- Doble de 8 bytes
    
- [signed] short [int] &ndash; utilizado para valores **booleanos** y números enteros 
    
- unsigned short [int]
    
- [signed long] int
    
### <a name="strings"></a>Cadenas

Todas las versiones de Excel:
  
- [signed] char \* &ndash; cadenas de bytes terminadas en null de hasta 255 caracteres 
    
- unsigned char \* &ndash; cadenas de bytes de longitud de hasta 255 caracteres 
    
A partir de Excel 2007:
  
- unsigned short \* &ndash; cadenas Unicode de hasta 32.767 caracteres de longitud o terminadas en null
    
Todos los números de la hoja de cálculo de Excel se almacenan como dobles para que no es necesario (y en realidad presenta una sobrecarga de conversión pequeña) declarar funciones de complemento como intercambiar tipos enteros con Excel.
  
Cuando usa tipos enteros, Excel comprueba que las entradas estén dentro de los límites del tipo y que produzcan errores con **#NUM!** si están fuera de dichos límites. La excepción es cuando se registra una función para un argumento **Booleano**, implementado con int corto En este caso, las entradas distintas de cero se convierte en 1 y cero se pasa directamente. 
  
## <a name="excel-specific-data-structures"></a>Estructuras de datos específicas de Excel

Todas las versiones de Excel:
  
- **FP** &ndash; una estructura de matriz con punto flotante bidimensional que admite hasta 65.356 filas por el número máximo de columnas admitidas en la versión determinada de Excel. 
    
- **XLOPER** &ndash; una estructura de varios tipos de datos que puede representar todos los tipos de datos de la hoja de cálculo (errores incluidos), enteros, referencias de rango, tipos de controles de flujo de hoja de macros XLM y un tipo de datos de almacenamiento binario interno. 
    
   > [!NOTE]
   > Las cadenas se representan como cadenas de bytes de longitud de hasta 255 caracteres.  
  
A partir de Excel 2007:
  
- **FP12** &ndash; una estructura de matriz con punto flotante bidimensional que admite todas las filas y columnas a partir de Excel 2007. 
    
- **XLOPER12** &ndash; una estructura de varios tipos de datos que se puede representar todos los tipos de datos de la hoja de cálculo (errores incluidos), enteros, referencias de rango, tipos de controles de flujo de hoja de macros XLM y un tipo de datos de almacenamiento binario interno. 
    
   > [!NOTE]
   > Las cadenas se representan como cadenas Unicode de longitud de hasta 32.767 caracteres.  
  
## <a name="registration-data-type-codes"></a>Códigos de tipos de datos de registro

Las funciones XLL se registran con la función de la API de C **xlfRegister**, que toma como tercer argumento una cadena de caracteres que codifica los tipos de argumento y de valor devuelto. Esta cadena también contiene la información que indica a Excel si la función es variable, es segura para subprocesos (a partir de Excel 2007), es equivalente a una hoja de macros y si devuelve el resultado al modificar un argumento en sitio.
  
La siguiente tabla se reproduce y se describe con más detalle en el tema [xlfRegister (Formulario 1)](xlfregister-form-1.md). Se reproduce aquí para proporcionar un contexto para el resto de esta sección. Por ejemplo, una función que toma una cadena Unicode de longitud (a partir de Excel 2007) se podría describir como tomar un tipo de argumento de C%. 
  
|Tipo de datos|Paso por valor|Paso por referencia (puntero)|Comentarios|
|:-----|:-----|:-----|:-----|
|Booleano  <br/> |A  <br/> |L  <br/> |short (0 = false o 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*   <br/> ||C, F  <br/> |Cadena de bytes en ASCII terminada en null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadena de bytes en ASCII de longitud  <br/> |
|unsigned short \* (a partir de Excel 2007)  <br/> ||C%, F%  <br/> |Cadena de caracteres anchos Unicode terminada en null  <br/> |
|unsigned short \* (a partir de Excel 2007)  <br/> ||D%, G%  <br/> |Cadena de caracteres anchos Unicode de longitud  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 bits  <br/> |
|Matriz  <br/> ||O  <br/> | Se pasa como tres argumentos por referencia:  <br/>1. \*filas short int  <br/>2. \*columnas short int  <br/>3. \*matriz double  <br/> |
|Matriz  <br/> (A partir de Excel 2007)  <br/> ||O%  <br/> | Se pasa como tres argumentos por referencia:  <br/>1. \*filas int  <br/>2. \*columnas int  <br/>3. \*matriz double  <br/> |
|FP  <br/> ||K  <br/> |Estructura de matriz con punto flotante  <br/> |
|FP12  <br/> (A partir de Excel 2007)  <br/> ||K%  <br/> |Estructura de matriz con punto flotante de cuadrícula grande  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||R  <br/> |Referencias de rango, matrices y valores  <br/> |
|XLOPER12  <br/> (A partir de Excel 2007)  <br/> ||Q  <br/> |Matrices y valores de la hoja de cálculo de tipo variable  <br/> |
|||U  <br/> |Referencias de rango, matrices y valores  <br/> |
   
Los tipos de **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q**, y **U** eran nuevos en Microsoft Office Excel 2007 y no son compatibles con versiones anteriores. Los tipos de cadena **F**, **F%**, **G**, y **G%** se usan para los argumentos modificados en sitio.  Cuando los argumentos **XLOPER** o **XLOPER12** se registran como tipo **P** o **Q** respectivamente, Excel convierte las referencias de celda única a valores simples y las referencias de varias celdas a matrices a la hora de prepararlas. 
  
Los tipos **P** y **Q** siempre llegan a la función como uno de los siguientes tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** o **xltypeNil**, pero no **xltypeRef ** o **xltypeSRef** porque a estas siempre se eliminan las referencias. 
  
El tipo **O**, que en realidad cuenta con tres argumentos en la pila, se introdujo para la compatibilidad con archivos DLL Fortran donde los argumentos se pasan por referencia. No puede usarlo para devolver un valor excepto declarar el argumento como valor devuelto que se modifica en sitio y colocando los resultados en los valores a los que se hace referencia. El tipo **O%** extiende el tipo **O** en Excel 2007 para que pueda acceder a matrices que tratan áreas más grandes que la cuadrícula de Office Excel 2003. 
  
## <a name="see-also"></a>Vea también

- [xlfRegister (Formulario 1)](xlfregister-form-1.md)
- [Conceptos de programación de Excel](excel-programming-concepts.md)
- [Referencia de funciones de API de SDK de XLL de Excel](excel-xll-sdk-api-function-reference.md)

