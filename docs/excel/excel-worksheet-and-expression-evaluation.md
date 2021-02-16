---
title: Hojas de cálculo y evaluación de expresiones de Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427769"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Hojas de cálculo y evaluación de expresiones de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El contenido de las celdas de la hoja de cálculo de Microsoft Excel se evalúa en uno de los cuatro tipos de datos básicos:
  
- **Numbers**
    
- **Boolean TRUE** o **FALSE**
    
- **Strings**
    
- **Errors**
    
Las matrices de tipos mixtos de estos tipos también se pueden introducir en fórmulas como argumentos para funciones o como valores que expanden más de una celda de una fórmula de matriz.
  
Cuando un usuario (o una macro de comandos) escribe algo en una celda, Excel intenta interpretar la entrada y muestra un mensaje de error si no puede. Si la entrada se empieza por un prefijo de cadena (una comilla simple), Excel coloca todos los caracteres de entrada en la celda tal como los proporciona, sin modificar. (El prefijo de cadena no se muestra). Si la entrada empieza por **=**, **+** o **-**, Excel intenta interpretar la entrada como una fórmula. Si la sintaxis es incorrecta o se detiene la evaluación, se muestra un error y la celda se pone en modo de edición. De lo contrario, Excel intenta identificar, convertir y evaluar los operadores y los nombres de la función, y sus argumentos. 
  
Antes de aplicar el operador, los operandos se evalúan de izquierda a derecha. Las funciones se evalúan a partir de los operadores de mayor prioridad y más internos (más anidados). Si los argumentos de función o los operandos no se pueden convertir a los tipos esperados, la evaluación produce un error y da como resultado un error **#VALUE!**. Cuando no se reconoce un token (que no es un valor literal) como una función, o un nombre o una etiqueta definida, la evaluación produce un error y da como resultado un error **#NAME?**. 
  
Si la entrada no empieza por cualquiera de estos, Excel comprueba los patrones conocidos de entrada, como fechas, horas, cantidades de moneda, porcentajes o números, y los interpreta según corresponda. Esto se hace de forma específica de la configuración regional. Si ninguna de estas interpretaciones tiene sentido, Excel vuelve a considerar la entrada como una cadena y la coloca en la celda sin cambiar.
  
Excel admite otros tipos de datos, el más visible de ellos es una referencia de rango. Excel convierte las referencias a los valores de las celdas a las que hace referencia al evaluar los argumentos para los operadores y las funciones que no toman argumentos de referencia, o cuando la expresión de una fórmula de celda se reduce a una referencia.
  
Excel expone la capacidad de reducir cualquier cadena de caracteres válidos a uno de los cuatro tipos de datos de hoja de cálculo básicos con **EVALUATE** de la función XLM y su equivalente de la API de C **xlfEvaluate**. Entre otras cosas, esta función proporciona una manera sencilla de evaluar los rangos con nombre en código de la DLL. Esta función difiere del comportamiento descrito anteriormente solo en que en lugar de mostrar mensajes de error o habilitar la edición de la celda, devuelve un error **#VALUE!** si se produce un error en la evaluación de la expresión. 
  
## <a name="numbers"></a>Números

Todos los números de hoja de cálculo de Excel se representan internamente como un número de punto flotante de precisión doble de 8 bytes, incluidos todos los enteros. Sin embargo, la implementación de estos números en Excel no es totalmente compatible con IEEE, como se muestra en la siguiente tabla.
  
|**Tipo**|**Máximo**|**Mínimo**|
|:-----|:-----|:-----|
|Doble de 8 bytes IEEE  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Hoja de cálculo (devuelto por la función o el valor de pegado)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Hoja de cálculo (entrada manual)  <br/> |9.99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
Los números de IEEE por debajo de lo normal (es decir, los números del rango 2,2250738585072009E \endash 308 4,9406564584124654E \endash 324) no se admiten en las hojas de cálculo de Excel, pero se admiten en los dobles de VBA.
  
Si una función DLL devuelve IEEE +/- infinity o un doble no válido, Excel lo convierte en **#NUM!**. Todos los números por debajo de lo normal y los números menores que el normal positivo mínimo de Excel se convierten en cero positivo. Se admite el cero negativo de IEEE, es decir, una función DLL lo puede devolver y se muestra como **-0**. (El operador **\<** no busca el cero negativo y, por lo tanto **=A1\<0** se evalúa como **TRUE** si A1 contiene un cero negativo). 
  
Tenga en cuenta que algunos formatos de número tienen límites más estrechos, por ejemplo, fechas y horas. La división de enteros es, de hecho, una división de número de punto flotante y puede, en casos extremos, dar un resultado no entero cuando el resultado preciso debería ser un entero.
  
## <a name="long-unicode-strings"></a>Cadenas Unicode largas

Todas las cadenas que el usuario ve en Excel, desde hace muchas versiones, se almacenan internamente como cadenas Unicode. Las cadenas de la hoja de cálculo de Unicode pueden ser de hasta 32.767 (2<sup>15</sup>- 1) caracteres de longitud y pueden contener cualquier carácter Unicode válido. 
  
Al introducir la API de C, las cadenas de hoja de cálculo eran cadenas de bytes limitadas a una longitud de 255 caracteres, y la API de C reflejaba estos límites. Con Excel 2007, la API de C se actualiza para controlar cadenas Unicode largas de Excel. Esto significa que funciones DLL registradas correctamente pueden aceptar argumentos Unicode y devolver las cadenas Unicode.
  
> [!NOTE]
> Las cadenas de bytes todavía se admiten totalmente en la API de C para la compatibilidad con versiones anteriores. Sin embargo, siguen teniendo el mismo límite de 255 caracteres. 
  
## <a name="returning-errors"></a>Devolver errores

Excel evalúa las celdas para buscar errores cuando no puede convertir los argumentos de función o de operador al tipo correcto, o si no reconoce una función o un nombre definido. Estos dos escenarios se describen anteriormente. Cuando los operadores y las funciones de hoja de cálculo integradas fallan, producen errores que informan al usuario del tipo de error. Debe hacer que las funciones de complemento devuelvan errores coherentes con el comportamiento en Excel.
  
### <a name="null"></a>#NULL!

Algunas funciones de información XML devuelven el error **#NULL!**. Por ejemplo, al llamar a **GET.DOCUMENT(78)** o a la función de la API de C equivalente **xlfGetDocument** con el argumento 78, cuando no hay resultados de impresoras instalados en este error que se devuelve. Algunas funciones también pueden devolverlos cuando, por ejemplo, evalúan una cadena vacía. 
  
Es posible que quiera devolver este error de la función de complemento cuando ninguno de los otros errores sea adecuado.
  
### <a name="div0"></a>#DIV/0!

El operador de división de Excel devuelve el error **#DIV/0!** cuando el denominador se evalúa en cero o un número es demasiado pequeño para ser representado como distinto de cero por Excel. Algunas funciones que, por definición, implican una división, también pueden devolver este error. Por ejemplo, **AVERAGE** devuelve este error si ninguna de las entradas se puede convertir a números. 
  
Solo debe considerar devolver este error desde la función de complemento para indicar que se detectó una división entre cero.
  
### <a name="value"></a>#VALUE!

Excel devuelve el error **#VALUE!** si una función o un argumento de operador no se puede convertir al tipo necesario. En el caso de los argumentos de función que no se pueden convertir, por ejemplo  `=LN("X")`, Excel no llama al código de función. Este es un punto que se debe recordar al escribir y depurar las funciones de complemento. 
  
Algunas funciones devuelven este error si no se puede convertir un argumento dentro del código de función. Por ejemplo,  `DATEVALUE("30-Feb-2007")` se produce este error a pesar de que el argumento es del tipo correcto. En este caso, es la función la que devuelve el error desde dentro de su código. Algunas funciones devuelven este error aunque se permitan los tipos de valor y los intervalos, por ejemplo  `FIND("a","xyz")` devuelve este error. 
  
Debe considerar devolver este error desde la función de complemento para indicar que los argumentos son del tipo incorrecto, no se pueden convertir al tipo correcto o están fuera del rango, aunque debe devolver **#NUM!** para los argumentos numéricos fuera del rango. También debe considerar devolver este error cuando los argumentos de rango o de matriz tienen el tamaño o la forma incorrectos. 
  
### <a name="ref"></a>#REF!

Excel genera el error **#REF!** dentro de una expresión cuando se copia en una ubicación donde la referencia relativa resultante queda fuera de los límites. Por ejemplo, si la celda B2 contiene la fórmula  `=A1`, copiarlo en la celda B1 da como resultado una fórmula **=#REF!**. Este error también se genera en las fórmulas que contienen una referencia que se sobrescribe en una operación de cortar y pegar, o se elimina de una fila, columna o eliminación de hoja de cálculo. Algunas funciones que pueden devolver referencias, pueden devolver este error, por ejemplo,  `OFFSET(A1,-1,-1)`. Los nombres de hoja de cálculo cuyas definiciones contienen referencias que dejan de ser válidas se evalúan para este error.
  
Si la función de complemento toma argumentos de referencia, considere devolver este error si las referencias no son válidas, o si pasa un error de referencia. La sección sobre XLOPER o XLOPER12 de [administración de memoria en Excel](memory-management-in-excel.md) describe cómo crear funciones que pueden aceptar y devolver argumentos de referencia. 
  
### <a name="name"></a>#NAME?

Excel genera el error **#NAME?** cuando una expresión contiene un token no reconocido como una función o un nombre definido. Si la función de complemento acceder a un nombre definido y no está definido, considere devolver este error. 
  
### <a name="num"></a>#NUM!

Muchas de las funciones matemáticas y numéricas integradas de Excel devuelven el error **#NUM!** cuando una entrada numérica está fuera del rango permitido, por ejemplo,  `LN(0)`. Considere devolver este error desde la función de complemento para indicar que una entrada numérica no era válida o estaba fuera del rango.
  
### <a name="na"></a>#N/A

A menudo se devuelve el error **#N/A** para indicar que un resultado correcto o significativo no está disponible. Por ejemplo, MATCH con el tercer cero de argumento devuelve este error si no se encuentra una coincidencia exacta. Este error también se puede generar con la función **NA** y se puede detectar específicamente con la función **ISNA**. Por lo tanto, es un error frecuente en hojas de cálculo para indicar un rango de condiciones específicas de la aplicación.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
[Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

