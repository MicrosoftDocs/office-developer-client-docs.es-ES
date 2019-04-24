---
title: Problemas conocidos en el desarrollo de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problemas conocidos [Excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304007"
---
# <a name="known-issues-in-excel-xll-development"></a>Problemas conocidos en el desarrollo de XLL de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En este tema se describen los problemas conocidos de Microsoft Excel que pueden surgir en el desarrollo de XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Anulación del registro de comandos y funciones XLL

Cuando un XLL registra una función o un comando, Excel crea un nuevo nombre para el recurso y asocia una referencia a la función DLL con ese nombre. El nombre se toma del cuarto argumento, *pxFunctionText* , de la función [xlfRegister](xlfregister-form-1.md) . Este nombre se oculta en los cuadros de diálogo normales para administrar los nombres de las hojas de cálculo. Para anular el registro de una función o un comando, debe eliminar el nombre mediante la función [xlfSetName](xlfsetname.md) , pasando el nombre pero sin pasar una definición. Sin embargo, un error impide que se elimine el nombre de las listas del Asistente para funciones. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>La cadena de Descripción del argumento se trunca en el Asistente para funciones

El parámetro *pxArgumentHelp1* y todos los parámetros subsiguientes de la función **xlfRegister** son cadenas opcionales que corresponden a los argumentos de la función XLL. El Asistente para funciones las muestra para proporcionar ayuda en el cuadro de diálogo de creación de argumentos. A veces Excel trunca la cadena correspondiente al argumento final en uno o dos caracteres cuando se muestra en el cuadro de diálogo. Para evitar esto, agregue una "cadena vacía" adicional como el último parámetro "ayuda de argumento" del registro de la función.
  
## <a name="binary-name-scope-limitation"></a>Limitación de ámbitos de nombre binario

Los nombres binarios y sus datos solo se pueden recuperar cuando la hoja de cálculo que estaba activa en el momento de crearse está activa de nuevo. Debido a que las funciones de hoja de cálculo no pueden activar hojas de cálculo dentro de un libro (solo los comandos pueden hacerlo), las aplicaciones de nombres binarios son muy limitadas. Si tiene un comando que solo se invoca desde una hoja de cálculo determinada, por ejemplo, puede usar un nombre binario para almacenar datos relacionados con el comando.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet y libros con fórmulas de matriz

En Excel 2003 y versiones anteriores, la [función xlSet](xlset.md) produce un error si intenta asignar valores a un rango de una hoja de cálculo que no es la hoja de cálculo activa, donde el rango equivalente de la hoja activa contiene una fórmula de matriz. En este caso, Excel muestra el mensaje "no se puede cambiar parte de una matriz". Esto se corrigió en Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Las referencias circulares se toleran en tablas de datos

Actualmente, Excel no genera un error si el cálculo en el que se basa una tabla de datos hace referencia a un elemento de la propia tabla. Como es improbable, debe tener cuidado al crear o modificar fórmulas que se usan para calcular los valores de la tabla de datos.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Conversión de un valor de XLOPER12 entero en XLOPER

Debido a que el tipo de entero **xltypeInt** es un entero con signo de 32 bits en el tipo de datos **XLOPER12** , pero solo es un entero de 16 bits con signo en el tipo de datos **XLOPER** , es posible que algunos valores enteros de **XLOPER12** no puedan estar contenidos en un **XLOPER**de entero. Cuando Excel convierte internamente este tipo, se soluciona este problema convirtiendo el tipo en un **XLOPER**de punto flotante **xltypeNum** .
  
La función [XLOper12ToXLOper](xloper12toxloper.md) de Framework refleja este comportamiento para que sea coherente con Excel internamente. Cuando se llama a esta función, no se debe suponer que el **XLOPER** devuelto siempre será **xltypeInt**; la lectura de **my_xloper. Val. w** proporciona un valor false si el tipo **my_xloper** es **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Devolución de XLOPER o XLOPER12 mediante la modificación de argumentos en su ubicación

Excel permite el registro de funciones que devuelven **XLOPER** o **XLOPER12** mediante la modificación de un argumento en su posición. Sin embargo, si un argumento **XLOPER**/ **XLOPER12** apunta a la memoria y, a continuación, se sobrescribe el puntero con el valor devuelto por la función dll, Excel puede perder memoria. Excel no muestra un error, pero puede que finalmente se bloquee. Además, si la DLL asignó memoria para el valor devuelto, es posible que Excel intente liberar dicha memoria, lo que podría provocar un bloqueo inmediato de la aplicación. Por lo tanto, no debe modificar los argumentos de**XLOPER12** de **XLOPER**/ en su lugar. Todos los argumentos **XLOPER** o **XLOPER12** deben tratarse como estrictamente de solo lectura. 
  
Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Vea también



[XLOper12ToXLOper](xloper12toxloper.md)


[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Administración de memoria en Excel](memory-management-in-excel.md)

