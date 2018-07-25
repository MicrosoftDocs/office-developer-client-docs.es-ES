---
title: Hojas de cálculo y evaluaci�n de expresiones de Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815608"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Evaluación de expresiones y hojas de cálculo de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El contenido de las celdas de la hoja de cálculo de Microsoft Excel se evalúa en uno de los cuatro tipos de datos básicos:
  
- **Numbers**
    
- **Boolean TRUE** o **FALSE**
    
- **Strings**
    
- **Errors**
    
Las matrices de tipos mixtos de estos tipos tambi�n se pueden introducir en fórmulas como argumentos para funciones o como valores que expanden m�s de una celda de una fórmula de matriz.
  
Cuando un usuario (o una macro de comandos) escribe algo en una celda, Excel intenta interpretar la entrada y muestra un mensaje de error si no puede. Si la entrada se empieza por un prefijo de cadena (una comilla simple), Excel coloca todos los caracteres de entrada en la celda tal como los proporciona, sin modificar. (El prefijo de cadena no se muestra). Si la entrada empieza por **=**, **+** o **-**, Excel intenta interpretar la entrada como una fórmula. Si la sintaxis es incorrecta o se detiene la evaluaci�n, se muestra un error y la celda se pone en modo de edici�n. De lo contrario, Excel intenta identificar, convertir y evaluar los operadores y los nombres de la función, y sus argumentos. 
  
Antes de aplicar el operador, los operandos se eval�an de izquierda a derecha. Las funciones se eval�an a partir de los operadores de mayor prioridad y m�s internos (m�s anidados). Si los argumentos de función o los operandos no se pueden convertir a los tipos esperados, la evaluaci�n produce un error y da como resultado un error **#VALUE!**. Cuando no se reconoce un token (que no es un valor literal) como una función, o un nombre o una etiqueta definida, la evaluaci�n produce un error y da como resultado un error **#NAME?**. 
  
Si la entrada no empieza por cualquiera de estos, Excel comprueba los patrones conocidos de entrada, como fechas, horas, cantidades de moneda, porcentajes o n�meros, y los interpreta seg�n corresponda. Esto se hace de forma espec�fica de la configuraci�n regional. Si ninguna de estas interpretaciones tiene sentido, Excel vuelve a considerar la entrada como una cadena y la coloca en la celda sin cambiar.
  
Excel admite otros tipos de datos, el m�s visible de ellos es una referencia de rango. Excel convierte las referencias a los valores de las celdas a las que hace referencia al evaluar los argumentos para los operadores y las funciones que no toman argumentos de referencia, o cuando la expresi�n de una fórmula de celda se reduce a una referencia.
  
Excel expone la capacidad de reducir cualquier cadena de caracteres v�lidos a uno de los cuatro tipos de datos de hoja de cálculo b�sicos con **EVALUATE** de la función XLM y su equivalente de la API de C **xlfEvaluate**. Entre otras cosas, esta función proporciona una manera sencilla de evaluar los rangos con nombre en códigode la DLL. Esta función difiere del comportamiento descrito anteriormente solo en que en lugar de mostrar mensajes de error o habilitar la edici�n de la celda, devuelve un error **#VALUE!** si se produce un error en la evaluaci�n de la expresi�n. 
  
## <a name="numbers"></a>Números

Todos los n�meros de hoja de cálculo de Excel se representan internamente como un n�mero de punto flotante de precisi�n doble de 8 bytes, incluidos todos los enteros. Sin embargo, la implementaci�n de estos n�meros en Excel no es totalmente compatible con IEEE, como se muestra en la siguiente tabla.
  
|**Tipo**|**M�ximo**|**M�nimo**|
|:-----|:-----|:-----|
|Doble de 8 bytes IEEE  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Hoja de cálculo (devuelto por la función o el valor de pegado)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Hoja de cálculo (entrada manual)  <br/> |9.99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
Los n�meros de IEEE por debajo de lo normal (es decir, los n�meros del rango 2,2250738585072009E \endash 308 4,9406564584124654E \endash 324) no se admiten en las hojas de cálculo de Excel, pero se admiten en los dobles de VBA.
  
Si una función DLL devuelve IEEE +/- infinity o un doble no v�lido, Excel lo convierte en **#NUM!**. Todos los n�meros por debajo de lo normal y los n�meros menores que el normal positivo m�nimo de Excel se convierten en cero positivo. Se admite el cero negativo de IEEE, es decir, una función DLL lo puede devolver y se muestra como **-0**. (El operador **\<** no busca el cero negativo y, por lo tanto **=A1\<0** se eval�a como **TRUE** si A1 contiene un cero negativo). 
  
Tenga en cuenta que algunos formatos de n�mero tienen l�mites m�s estrechos, por ejemplo, fechas y horas. La divisi�n de enteros es, de hecho, una divisi�n de n�mero de punto flotante y puede, en casos extremos, dar un resultado no entero cuando el resultado preciso deber�a ser un entero.
  
## <a name="long-unicode-strings"></a>Cadenas Unicode largas

Todas las cadenas que el usuario ve en Excel, desde hace muchas versiones, se almacenan internamente como cadenas Unicode. Las cadenas de la hoja de cálculo de Unicode pueden ser de hasta 32.767 (2<sup>15</sup>-�1) caracteres de longitud y pueden contener cualquier car�cter Unicode v�lido. 
  
Al introducir la API de C, las cadenas de hoja de cálculo eran cadenas de bytes limitadas a una longitud de 255 caracteres, y la API de C reflejaba estos l�mites. Con Excel 2007, la API de C se actualiza para controlar cadenas Unicode largas de Excel. Esto significa que funciones DLL registradas correctamente pueden aceptar argumentos Unicode y devolver las cadenas Unicode.
  
> [!NOTE]
> Las cadenas de bytes todav�a se admiten totalmente en la API de C para la compatibilidad con versiones anteriores. Sin embargo, siguen teniendo el mismo l�mite de 255 caracteres. 
  
## <a name="returning-errors"></a>Devolver errores

Excel eval�a las celdas para buscar errores cuando no puede convertir los argumentos de función o de operador al tipo correcto, o si no reconoce una función o un nombre definido. Estos dos escenarios se describen anteriormente. Cuando los operadores y las funciones de hoja de cálculo integradas fallan, producen errores que informan al usuario del tipo de error. Debe hacer que las funciones de complemento devuelvan errores coherentes con el comportamiento en Excel.
  
### <a name="null"></a>#NULL!

Algunas funciones de información XML devuelven el error **#NULL!**. Por ejemplo, al llamar a **GET.DOCUMENT(78)** o a la función de la API de C equivalente **xlfGetDocument** con el argumento 78, cuando no hay resultados de impresoras instalados en este error que se devuelve. Algunas funciones tambi�n pueden devolverlos cuando, por ejemplo, eval�an una cadena vac�a. 
  
Es posible que quiera devolver este error de la función de complemento cuando ninguno de los otros errores sea adecuado.
  
### <a name="div0"></a>#DIV/0!

El operador de divisi�n de Excel devuelve el error **#DIV/0!** cuando el denominador se eval�a en cero o un n�mero es demasiado peque�o para ser representado como distinto de cero por Excel. Algunas funciones que, por definici�n, implican una divisi�n, tambi�n pueden devolver este error. Por ejemplo, **AVERAGE** devuelve este error si ninguna de las entradas se puede convertir a n�meros. 
  
Solo debe considerar devolver este error desde la función de complemento para indicar que se detect� una divisi�n entre cero.
  
### <a name="value"></a>#VALUE!

Excel devuelve el error **#VALUE!** si una función o un argumento de operador no se puede convertir al tipo necesario. En el caso de los argumentos de función que no se pueden convertir, por ejemplo  `=LN("X")`, Excel no llama al códigode función. Este es un punto que se debe recordar al escribir y depurar las funciones de complemento. 
  
Algunas funciones devuelven este error si no se puede convertir un argumento dentro del códigode función. Por ejemplo,  `DATEVALUE("30-Feb-2007")` se produce este error a pesar de que el argumento es del tipo correcto. En este caso, es la función la que devuelve el error desde dentro de su código. Algunas funciones devuelven este error aunque se permitan los tipos de valor y los intervalos, por ejemplo  `FIND("a","xyz")` devuelve este error. 
  
Debe considerar devolver este error desde la función de complemento para indicar que los argumentos son del tipo incorrecto, no se pueden convertir al tipo correcto o est�n fuera del rango, aunque debe devolver **#NUM!** para los argumentos num�ricos fuera del rango. Tambi�n debe considerar devolver este error cuando los argumentos de rango o de matriz tienen el tama�o o la forma incorrectos. 
  
### <a name="ref"></a>#REF!

Excel genera el error **#REF!** dentro de una expresi�n cuando se copia en una ubicaci�n donde la referencia relativa resultante queda fuera de los l�mites. Por ejemplo, si la celda B2 contiene la fórmula  `=A1`, copiarlo en la celda B1 da como resultado una fórmula **=#REF!**. Este error tambi�n se genera en las fórmulas que contienen una referencia que se sobrescribe en una operaci�n de cortar y pegar, o se elimina de una fila, columna o eliminaci�n de hoja de cálculo. Algunas funciones que pueden devolver referencias, pueden devolver este error, por ejemplo,  `OFFSET(A1,-1,-1)`. Los nombres de hoja de cálculo cuyas definiciones contienen referencias que dejan de ser v�lidas se eval�an para este error.
  
Si la función de complemento toma argumentos de referencia, considere devolver este error si las referencias no son v�lidas, o si pasa un error de referencia. La secci�n sobre XLOPER o XLOPER12 de [administración de memoria en Excel](memory-management-in-excel.md) describe c�mo crear funciones que pueden aceptar y devolver argumentos de referencia. 
  
### <a name="name"></a>#NAME?

Excel genera el error **#NAME?** cuando una expresi�n contiene un token no reconocido como una función o un nombre definido. Si la función de complemento acceder a un nombre definido y no est� definido, considere devolver este error. 
  
### <a name="num"></a>#NUM!

Muchas de las funciones matem�ticas y num�ricas integradas de Excel devuelven el error **#NUM!** cuando una entrada num�rica est� fuera del rango permitido, por ejemplo,  `LN(0)`. Considere devolver este error desde la función de complemento para indicar que una entrada num�rica no era v�lida o estaba fuera del rango.
  
### <a name="na"></a>#N/A

A menudo se devuelve el error **#N/A** para indicar que un resultado correcto o significativo no est� disponible. Por ejemplo, MATCH con el tercer cero de argumento devuelve este error si no se encuentra una coincidencia exacta. Este error tambi�n se puede generar con la función **NA** y se puede detectar espec�ficamente con la función **ISNA**. Por lo tanto, es un error frecuente en hojas de cálculo para indicar un rango de condiciones espec�ficas de la aplicación.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
  
[Evaluaci�n de nombres y otras expresiones de fórmula de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

