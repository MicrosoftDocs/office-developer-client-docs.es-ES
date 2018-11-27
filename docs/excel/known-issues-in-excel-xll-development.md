---
title: Problemas conocidos en el desarrollo de XLL de Excel
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
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685182"
---
# <a name="known-issues-in-excel-xll-development"></a>Problemas conocidos en el desarrollo de XLL de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En este tema se describe los problemas conocidos de Microsoft Excel que pueden surgir en el desarrollo de XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Anulando el registro de los comandos XLL y funciones

Cuando registra un XLL una función o un comando, Excel crea un nuevo nombre para el recurso y asocia una referencia a la función DLL con ese nombre. Se toma el nombre del cuarto argumento, *pxFunctionText* , de la función [xlfRegister](xlfregister-form-1.md) . Este nombre se oculta de los cuadros de diálogo normal para administrar los nombres de hoja de cálculo. Para anular el registro de una función o un comando, debe eliminar el nombre mediante el uso de la función [xlfSetName](xlfsetname.md) , pasando el nombre pero no pasando una definición. Sin embargo, un error Esto impide quitar el nombre de las listas del Asistente para la función. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Truncamiento de cadena de argumento descripción en el Asistente para funciones

El parámetro *pxArgumentHelp1* y todos los parámetros posteriores de la función **xlfRegister** son cadenas opcionales que se corresponden con los argumentos de la función XLL. El Asistente para la función muestra estos para proporcionar ayuda en el cuadro de diálogo de construcción de argumento. A veces Excel trunca la cadena que corresponde al argumento final por uno o dos caracteres cuando se muestra en el cuadro de diálogo. Se puede evitar mediante la adición de una adicional "cadena vacía" como el último parámetro "Ayuda argumento" del registro (función).
  
## <a name="binary-name-scope-limitation"></a>Limitación del ámbito de nombre del archivo binario

Nombres binario y los datos se pueden recuperar sólo cuando la hoja de cálculo que estaba activa en el momento en que se crearon nuevo está activo. Debido a que las funciones de hoja de cálculo no pueden activar las hojas de cálculo dentro de un libro (solo comandos pueden hacerlo), aplicaciones de nombres binarios son muy limitadas. Si dispone de un comando que sólo se invoca desde una hoja de cálculo determinada, por ejemplo, podría usar un nombre del archivo binario para almacenar los datos relacionados con el comando.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet y libros con fórmulas de matriz

En Excel 2003 y versiones anteriores, la [función xlSet](xlset.md) genera un error si se intenta asignar valores en un rango de una hoja de cálculo que no es la hoja de cálculo activa, donde el intervalo equivalente en la hoja activa contiene una fórmula de matriz. En este caso, Excel muestra el mensaje "No se puede cambiar parte de una matriz." Esto se ha solucionado en Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Las referencias circulares se tolerarán en tablas de datos

Actualmente Excel no provoca un error si el cálculo basado en una tabla de datos hace referencia a algo en la propia tabla. Como poco probable como es posible que en este escenario, debe tener cuidado cuando se está creando o modificando las fórmulas que se utilizan para calcular los valores de tabla de datos.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Conversión de un número entero XLOPER12 a un XLOPER

Debido a que el tipo de entero **xltypeInt** es un entero con signo de 32 bits en el tipo de datos **XLOPER12** , pero es sólo un entero con signo de 16 bits en el tipo de datos **XLOPER** , es posible que algunos valores de **XLOPER12** entero no pueden estar incluidos en un número entero **XLOPER**. Donde Excel convierte este tipo internamente, obtiene este problema mediante la conversión del tipo a un punto flotante **xltypeNum** **XLOPER**.
  
La función de Framework [XLOper12ToXLOper](xloper12toxloper.md) refleja este comportamiento para que sea coherente con Excel internamente. Cuando se llama a esta función, no debe asumir que el devuelto **XLOPER** siempre será **xltypeInt**; lectura de **my_xloper.val.w** proporciona un valor false si el tipo de **my_xloper** es **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Devolver XLOPER o XLOPER12 mediante la modificación de argumentos en contexto

Excel permite el registro de las funciones que devuelven un **XLOPER** o **XLOPER12** mediante la modificación de un argumento en su lugar. Sin embargo, si un **XLOPER**/ puntos de argumento**XLOPER12** a la memoria y el puntero a continuación, se sobrescribe con el valor devuelto de la función DLL, Excel puede perder memoria. Excel no muestra un error, pero podría bloquearse al final. Además, si el archivo DLL de memoria asignada para el valor devuelto, Excel intenta liberar esa memoria, lo que puede provocar un bloqueo de la aplicación inmediato. Por lo tanto, no se debe modificar **XLOPER**/ **XLOPER12** argumentos en su lugar. Argumentos de todos los **XLOPER** o **XLOPER12** deben tratarse como sólo lectura. 
  
Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Vea tambi�n



[XLOper12ToXLOper](xloper12toxloper.md)


[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)
  
[Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Administración de memoria en Excel](memory-management-in-excel.md)

