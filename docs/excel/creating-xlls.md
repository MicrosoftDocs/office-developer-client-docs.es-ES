---
title: Creación de XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- archivos DLL [excel 2007], llamada a excel, xlAutoFree (función) [Excel 2007], [Excel 2007],xlcall32.lib [Excel 2007], [Excel 2007],xlcall.cpp [Excel 2007], xlAutoRemove (función) [Excel 2007], xlAddInManagerInfo (función) xlAutoRegister (función) xlAutoFree12 función [Excel 2007], xlAutoAdd (función) [Excel 2007], xlAutoOpen (función) [Excel 2007], xlAutoClose (función) [Excel 2007], archivos DLL [Excel 2007], convirtiendo en XLL, XLL [Excel 2007], llamada a Excel, xlAutoRegister12 (función) [Excel 2007],xlcall.h [Excel función de xlAddInManagerInfo12 de 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: de347d34768c25adf0d96642b4fade781ae26a9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815535"
---
# <a name="creating-xlls"></a>Creación de XLL

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Si el archivo DLL es autónoma o se basa únicamente en otras bibliotecas, debe conocer cómo habilitar Microsoft Excel tener acceso a sus funciones y comandos. Para obtener más información, vea [Archivos DLL de Access en Excel](how-to-access-dlls-in-excel.md). 
  
Sin embargo, si el archivo DLL necesita tener acceso a funcionalidad de Excel (por ejemplo, para obtener el contenido de una celda, para llamar a una función de hoja de cálculo, o para consultar Excel para obtener información del área de trabajo), el código debe ser capaz de devolver la llamada en Excel.
  
La API de C de Excel proporciona varias funciones que les permiten a las DLL devolver la llamada en Excel. Para obtener acceso a estos, el archivo DLL debe estar vinculado estáticamente en tiempo de compilación con la biblioteca de Excel 32-bit, xlcall32.lib. La biblioteca estática es que se pueden descargar de Microsoft como parte del SDK de XLL de Microsoft Excel 2013, que incluye las versiones de 32 bits y 64 bits de esta biblioteca.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Habilitación de la DLL de devolución de llamada a Excel

Para un archivo DLL para poder tener acceso a la funcionalidad de Excel y obtener o establecer la información del área de trabajo, primero debe obtener las direcciones de las funciones de devolución de llamada de Excel **Excel4**, **Excel4v**, **Excel12**y **Excel12v**. Los dos últimos se introdujeron en Excel 2007 y están disponibles en versiones posteriores. Para obtener acceso a todos ellos, el proyecto de archivo DLL debe incluir las referencias a los siguientes archivos desde el SDK de XLL de Excel de 2013. Si desea obtener acceso sólo las dos primeras devoluciones de llamada (en cualquier versión de Excel), el proyecto debe incluir sólo los dos primeros archivos.
  
### <a name="xlcallh"></a>Xlcall.h

El archivo Xlcall.h contiene los siguientes elementos:
  
- Prototipos de función para todas las funciones de devolución de llamada.
    
- Definiciones de las estructuras de datos que las devoluciones de llamada que se usan para intercambiar datos entre el archivo DLL o XLL y Excel y las definiciones de constantes de tipo de datos.
    
- Definiciones de los equivalentes de función y el comando de API de C de la hoja de cálculo, las funciones de hoja de macros y comandos admitidos de Excel.
    
- Definiciones de función de devolución de llamada devuelven valores.
    
Debe utilizar el **#include** la directiva para este archivo, directa o indirectamente a través de otro archivo de encabezado, en todos los archivos que obtener acceso a la API de C o que controlar los tipos de datos que utiliza la API de C. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

La biblioteca de Xlcall32.lib exporta las dos primeras devoluciones de llamada, **Excel4** y **Excel4v**y también la función **XlCallVer** . Sin una referencia a esta biblioteca en el proyecto, el vinculador no puede crear el XLL si ha usado cualquiera de estas devoluciones de llamada en el código. (Puede obtener las direcciones de estas funciones si vincula dinámicamente a la Xlcall32.dll equivalente a la que se copian en el sistema como parte de una instalación normal de Excel). 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

No se exportan las devoluciones de llamada de Excel **Excel12** y **Excel12v** en Xlcall32.lib. Esto garantiza que los proyectos XLL que se crea a partir de Excel 2007 también funciona con versiones anteriores de Excel. El módulo Xlcall.cpp contiene código para la **Excel12** y **Excel12v** funciones, que llaman a una entrada de Excel elija Iniciar en Excel 2007, o devuelven un valor de error seguros si está ejecutando una versión anterior de Excel. Debe incluir este módulo en el proyecto si desea crear un XLL que ejecuta a partir de Excel 2007 y que es capaz de usar los nuevos tipos de datos que administran las cuadrículas más grandes y cadenas Unicode más largas. 
  
> [!NOTE]
> Iniciar con el SDK de Excel 2010, se puede compilar este archivo para los XLL de 32 bits y 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Cómo convertir archivos DLL en XLL: Administrador de funciones de la interfaz de complemento

Un XLL es un archivo DLL que se exporta varios procedimientos que son llamados por Excel o el Administrador de complementos de Excel. Estos procedimientos se describe brevemente aquí y se analizan detalladamente en [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md). Todas estas devoluciones de llamada DLL empiece con el prefijo **xlAuto**. Sólo uno de ellos, el comando **xlAutoOpen**, es necesario. Se llama cuando el complemento se activa y se utiliza normalmente para registrar funciones XLL y comandos con Excel y realizar otras tareas de inicialización. Las firmas de función y las implementaciones de ejemplo de todas las funciones **xlAuto** se proporcionan en secciones posteriores. 
  
Aunque **xlAutoOpen** es la única necesaria de estas devoluciones de llamada, el complemento es posible que también necesite exportar otros usuarios según su comportamiento. 
  
Excel 2007 introdujo un nuevo tipo de datos, **XLOPER12**, para dar cabida a las cuadrículas más grandes y para admitir cadenas largas de Unicode. **XLOPER12** se describe más adelante en este tema. Mientras que funciones **xlAuto** toman o devuelven el tipo de datos anterior **XLOPER**, nuevas versiones de estas funciones se introdujeron en Excel 2007 que usan tipos de datos **XLOPER12** . Con la excepción de **xlAutoFree12**, que a veces se debe implementar para evitar **XLOPER12** memoria pérdidas, puede omitir sin ningún riesgo todas la versión 12 funciones **xlAuto** , en cuyo caso, empezando en Excel 2007, las llamadas de Excel **XLOPER** versiones. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel llama a la función [xlAutoOpen](xlautoopen.md) cada vez que se activa el XLL. El complemento se activará en el inicio de una sesión de Excel si estaba activo en la última sesión de Excel que finalizó normalmente. El complemento se activa si se carga durante una sesión de Excel. El complemento se puede desactivar y reactivar una durante una sesión de Excel, y se llama a la función de reactivación. 
  
Debe usar **xlAutoOpen** para registrar los comandos y funciones XLL, inicializar las estructuras de datos, personalizar la interfaz de usuario y así sucesivamente. 
  
Si el complemento implementa y exporta la función [xlAutoRegister](xlautoregister-xlautoregister12.md) o la función [xlAutoRegister12](xlautoregister-xlautoregister12.md) , Excel puede intentar activar y registrar un comando o función sin llamar primero a la función **xlAutoOpen** . En este caso, debe asegurarse de que el complemento está lo suficientemente inicializado para que su función o el comando para que funcione correctamente. Si no es así, se debe ya sea producirá un error en el intento para registrar la función o el comando, o realizar la inicialización necesaria. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel llama a la función [xlAutoClose](xlautoclose.md) cada vez que se desactiva el XLL. El complemento se desactivará cuando finaliza una sesión de Excel normalmente. Si el usuario desactiva el complemento durante una sesión de Excel, se llama a la función. 
  
Debe usar **xlAutoClose** para anular el registro de las funciones y comandos, liberar recursos, deshacer las personalizaciones y así sucesivamente. 
  
> [!NOTE]
> Hay un problema conocido con la anulación del registro de las funciones y comandos. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel llama a la [función xlAutoAdd](xlautoadd.md) cada vez que el usuario activa el XLL durante una sesión de Excel mediante el uso del administrador. Esta función no se llama cuando Excel se inicia y carga un complemento preinstalado. 
  
Puede usar esta función para mostrar un cuadro de diálogo personalizado que indica al usuario que se ha activado el complemento, para leer o escribir en el registro o para comprobar la información de licencias.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel llama a la función [xlAutoRemove](xlautoremove.md) cada vez que el usuario desactiva el XLL durante una sesión de Excel mediante el uso del administrador. Esta función no se llama cuando se cierra una sesión de Excel, normalmente o de forma anómala, con el complemento instalado. 
  
Puede usar esta función para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha desactivado, o para leer o escribir en el registro.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel llama a la función [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) cuando se invoca el Administrador de complementos por primera vez en una sesión de Excel. Si Excel pasa un argumento igual a 1, esta función debe devolver una cadena (normalmente, el nombre del complemento) de lo contrario, debe devolver **#VALUE!**.
  
Iniciar en Excel 2007, Excel llama a la función **xlAddInManagerInfo12** preferencia a la función **xlAddInManagerInfo** si lo exporta el XLL. La función **xlAddInManagerInfo12** debe trabajar en la misma manera que la función **xlAddInManagerInfo** para evitar las diferencias específicas de la versión en el comportamiento de los XLL. La función **xlAddInManagerInfo12** debe devolver un tipo de datos **XLOPER12** , mientras que la función **xlAddInManagerInfo** debe devolver un tipo de datos **XLOPER** . 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel llama a la función [xlAutoRegister](xlautoregister-xlautoregister12.md) cada vez que se ha realizado una llamada a la función XLM **registrar**o la función de API de C equivalente [xlfRegister](xlfregister-form-1.md) , con la devolución y tipos de argumento falta para la función que se está registrada. La función **xlAutoRegister** permite el XLL buscar sus listas internas de funciones exportadas y comandos para registrar la función con el argumento y devolver los tipos especificados. 
  
Iniciar en Excel 2007, Excel llama a la función **xlAddInRegister12** preferencia a la función **xlAddInRegister** si lo exporta el XLL. 
  
> [!NOTE]
> Si **xlAddInRegister**/ **xlAddInRegister12** intenta registrar la función sin proporcionar el argumento y devolver tipos, una recursiva al llamar a bucle se produce que finalmente desbordamientos de la pila de llamadas y hace que Excel cerrar o detener responder. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel llama a la función [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) justo después de que una función de hoja de cálculo XLL devuelve un **XLOPER**/ tipo de datos de**XLOPER12** con un conjunto de marca que indica a Excel hay memoria que el XLL debe liberar aún. Esto permite que el XLL devolver dinámicamente asignado matrices, cadenas y las referencias externas a la hoja de cálculo sin pérdidas de memoria. Iniciar en Excel 2007, se admite el tipo de datos **XLOPER12** . Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).
  
> [!NOTE]
> Iniciar en Excel 2007, cuando Excel está configurada para usar recálculo de hoja de cálculo multiproceso, la **xlAutoFree**/ **xlAutoFree12** función se llama en el mismo subproceso que simplemente se usó para llamar a la función que se devuelve. La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que todas las celdas de la hoja de cálculo subsiguientes se evalúan en ese subproceso. Esto simplifica el diseño de subprocesos en su XLL. Para obtener más información, vea [Nuevo cálculo multiproceso en Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Creación de XLL de 64 bits

Excel y funciones definidas por el usuario pueden ejecutar en sistemas operativos de 64 bits para aprovechar las ventajas de rendimiento sobre los sistemas operativos de 32 bits. Excel pasa valores en estructuras **XLOPER12** que incluyen información acerca de los tipos de los datos. Preste atención al convertir entre valores de la estructura de **XLOPER12** y tipos nativos como **int** o punteros para conservar los valores en el tipo de mayor tamaño. 
  
## <a name="see-also"></a>Ver también



[Funciones XLL de llamada desde el Asistente para la función o cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Administrador de complementos y funciones de la interfaz XLL](add-in-manager-and-xll-interface-functions.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

