---
title: Problemas conocidos en Excel desarrollo XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problemas conocidos [excel 2007]
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
# <a name="known-issues-in-excel-xll-development"></a>Problemas conocidos en Excel desarrollo XLL

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En este tema se describen los problemas conocidos Microsoft Excel que se pueden encontrar en el desarrollo de XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Anular el registro de comandos y funciones XLL

Cuando un XLL registra una función o un comando, Excel crea un nuevo nombre para el recurso y asocia una referencia a la función DLL con ese nombre. El nombre se toma del cuarto argumento, *pxFunctionText* , de la [función xlfRegister.](xlfregister-form-1.md) Este nombre está oculto en los cuadros de diálogo normales para administrar nombres de hoja de cálculo. Para anular el registro de una función o comando, debe eliminar el nombre mediante la función [xlfSetName,](xlfsetname.md) pasando el nombre pero sin pasar una definición. Sin embargo, un error impide que se quite el nombre de las listas del Asistente para funciones. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Truncamiento de cadenas de descripción de argumentos en el Asistente para funciones

El  *parámetro pxArgumentHelp1*  y todos los parámetros subsiguientes de la función **xlfRegister** son cadenas opcionales que corresponden a los argumentos de la función XLL. El Asistente para funciones las muestra para proporcionar ayuda en el cuadro de diálogo de construcción de argumentos. A Excel trunca la cadena que corresponde al argumento final por uno o dos caracteres al mostrarla en el cuadro de diálogo. Puede evitar esto agregando una "cadena vacía" adicional como el último parámetro "ayuda de argumento" del registro de la función.
  
## <a name="binary-name-scope-limitation"></a>Limitación de ámbito de nombre binario

Los nombres binarios y sus datos solo se pueden recuperar cuando la hoja de cálculo que estaba activa en el momento en que se crearon está de nuevo activa. Dado que las funciones de hoja de cálculo no pueden activar hojas de cálculo dentro de un libro (solo los comandos pueden hacerlo), las aplicaciones de nombres binarios son muy limitadas. Si tiene un comando que solo se invoca desde una hoja de cálculo determinada, por ejemplo, podría usar un nombre binario para almacenar datos relacionados con comandos.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet y Libros con fórmulas de matriz

En Excel 2003 y versiones anteriores, la función [xlSet](xlset.md) produce un error si intenta asignar valores a un rango de una hoja de cálculo que no es la hoja de cálculo activa, donde el rango equivalente de la hoja activa contiene una fórmula de matriz. En este caso, Excel muestra el mensaje "No se puede cambiar parte de una matriz". Esto se corrigió en Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Las referencias circulares se toleran en tablas de datos

Excel genera actualmente un error si el cálculo en el que se basa una tabla de datos hace referencia a algo de la propia tabla. Por poco probable que sea este escenario, debe tener cuidado al crear o modificar fórmulas que se usan para calcular valores de tabla de datos.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Convertir un número entero XLOPER12 en un XLOPER

Dado que el tipo de entero **xltypeInt** es un entero con signo de 32 bits en el tipo de datos **XLOPER12,** pero solo es un entero con signo de 16 bits en el tipo de datos **XLOPER,** es posible que algunos valores enteros **XLOPER12** no se puedan contener en un **entero XLOPER**. Donde Excel convierte este tipo internamente, se obtiene alrededor de este problema convirtiendo el tipo en un **xltypeNum** **XLOPER de** punto flotante.
  
La función [XLOper12ToXLOper](xloper12toxloper.md) de Framework refleja este comportamiento para que sea coherente con Excel internamente. Al llamar a esta función, no debe asumir que **el XLOPER** devuelto siempre será **xltypeInt**; leer **my_xloper.val.w** proporciona un valor false si el **tipo my_xloper** es **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Devolver XLOPER o XLOPER12 modificando argumentos en su lugar

Excel permite el registro de funciones que devuelven **un XLOPER** o **XLOPER12** modificando un argumento en su lugar. Sin embargo, si un argumento /  **XLOPER XLOPER12** apunta a la memoria y, a continuación, el valor devuelto de la función DLL sobrescribe el puntero, Excel pérdida de memoria. Excel no muestra un error, pero puede que finalmente se bloquea. Además, si el DLL asignó memoria para el valor devuelto, Excel podría intentar liberar esa memoria, lo que podría provocar un bloqueo inmediato de la aplicación. Por lo tanto, no debe modificar **los argumentos** /  **XLOPER XLOPER12** en su lugar. Todos **los argumentos XLOPER** **o XLOPER12** deben tratarse como de sólo lectura estrictamente. 
  
Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Vea también



[XLOper12ToXLOper](xloper12toxloper.md)


[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Administración de memoria en Excel](memory-management-in-excel.md)

