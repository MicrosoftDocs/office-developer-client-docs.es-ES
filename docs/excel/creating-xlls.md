---
title: Crear XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], llamar a la función excel,xlAutoFree [Excel 2007], función xlAutoFree12 [Excel 2007], xlcall32.lib [Excel 2007], función xlAutoRegister [Excel 2007], xlcall.cpp [Excel 2007], función xlAutoRemove [Excel 2007], función xlAddInManagerInfo [Excel 2007], función xlAutoAdd [Excel 2007], función xlAutoOpen [Excel 2007], función xlAutoClose [Excel 2007],DLLs [Excel 2007], convertir en XLL,XLL [Excel 2007], llamar a la función Excel,xlAutoRegister12 [Excel 2007],xlcall.h [Excel 2007], función xlAddInManagerInfo12 [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304147"
---
# <a name="creating-xlls"></a>Crear XLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Si tu DLL es autónoma o se basa en otras bibliotecas, debes saber cómo habilitar el acceso de Microsoft Excel a sus funciones y comandos. Para obtener más información, consulta [Acceder a DLL en Excel](how-to-access-dlls-in-excel.md). 
  
Sin embargo, si tu DLL necesita tener acceso a las funciones de Excel (por ejemplo, para obtener el contenido de una celda, llamar a una función de hoja de cálculo o interrogar a Excel para obtener la información del área de trabajo), el código debe ser capaz de devolver la llamada a Excel.
  
La API de C de Excel proporciona varias funciones que permiten a las DLL devolver la llamada a Excel. Para acceder a ellas, la DLL debe estar vinculada de forma estática en tiempo de compilación con la biblioteca de Excel de 32 bits, xlcall32.lib. La biblioteca estática se puede descargar de Microsoft como parte del SDK de XLL de Microsoft Excel 2013, que incluye las versiones de 32 bits y 64 bits de esta biblioteca.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Habilitar la DLL para devolver la llamada a Excel

Para que un archivo DLL pueda obtener acceso a las funciones de Excel y obtener o establecer información del área de trabajo, primero debe obtener las direcciones de las funciones de retrollamada de Excel **Excel4**, **Excel4v**, ** Excel12** y **Excel12v**. Las dos últimas se introdujeron en Excel 2007 y están disponibles en versiones posteriores. Para obtener acceso a todas ellas, el proyecto DLL debe incluir referencias a los siguientes archivos de SDK de XLL de Excel 2013. Si deseas tener acceso solo a las dos primeras retrollamadas (en cualquier versión de Excel), tu proyecto solo debe incluir los dos primeros archivos.
  
### <a name="xlcallh"></a>Xlcall.h

El archivo Xlcall.h contiene los siguientes elementos:
  
- Prototipos de función para todas las funciones de retrollamada.
    
- Definiciones de las estructuras de datos que usan las retrollamadas para intercambiar datos entre DLL/XLL y Excel, y definiciones de constantes de tipo de datos.
    
- Definiciones de los equivalentes de función y comando de C de API de la hoja de cálculo, funciones de hoja de macros y comandos de Excel admitidos.
    
- Definiciones de los valores devueltos de la función de retrollamada.
    
Debes usar la directiva **#incluir** para este archivo, directa o indirectamente a través de otro archivo de encabezado, en todos los archivos que tienen acceso a la API de C o que controlan los tipos de datos que usa la API de C. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

La biblioteca Xlcall32.lib exporta las dos primeras retrollamadas, **Excel4** y **Excel4v**así como la función **XlCallVer**. Sin una referencia a esta biblioteca en tu proyecto, el vinculador no puede crear el XLL si usaste alguna de estas retrollamadas en tu código. (Puedes obtener las direcciones de estas funciones mediante un vínculo dinámico al archivo Xlcall32.dll equivalente que se copia en tu sistema como parte de una instalación de Excel normal). 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Las retrollamadas **Excel12** y **Excel12v** de Excel no se exportan en Xlcall32.lib. Así se garantiza que los proyectos XLL que creas a partir de Excel 2007 también funcionen con versiones anteriores de Excel. El módulo Xlcall.cpp contiene el código para las funciones de **Excel12** y **Excel12v**, que llaman a un punto de entrada de Excel a partir de Excel 2007, o devuelven un valor de error seguro si estás ejecutando una versión anterior de Excel. Si deseas crear un XLL que se ejecuta a partir de Excel 2007 y que es capaz de usar los nuevos tipos de datos que administran las cuadrículas más grandes y cadenas Unicode más largas, debes incluir este módulo en tu proyecto. 
  
> [!NOTE]
> Empezando con el SDK de Excel 2010, este archivo se puede compilar para XLL de 32 y 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Cómo convertir DLL en XLL: funciones de la interfaz del administrador de complementos

Un XLL es un archivo DLL que exporta varios procedimientos llamados por Excel o el administrador de complementos de Excel. Estos procedimientos se describen brevemente aquí y se explican en detalle en las [funciones de la interfaz del administrador de complementos y XLL](add-in-manager-and-xll-interface-functions.md). Todas estas retrollamadas de DLL comienzan con el prefijo **xlAuto**. Solo una de ellas, el comando **xlAutoOpen**, es necesaria. Se la llama cuando el complemento está activado y se usa normalmente para registrar funciones y comandos XLL con Excel y para realizar otras tareas de inicialización. Las firmas de función e implementación de ejemplos de todas las funciones **xlAuto** se proporcionan en las secciones posteriores. 
  
Aunque **xlAutoOpen** es la única retrollamada requerida, tu complemento puede necesitar exportar otras según su comportamiento. 
  
Excel 2007 introdujo un nuevo tipo de datos, **XLOPER12**, para dar cabida a las cuadrículas más grandes y admitir cadenas largas de Unicode. **XLOPER12** se describe más adelante en este tema. Si bien las funciones **xlAuto** toman o devuelven el tipo de datos antiguos **XLOPER**, se introdujeron nuevas versiones de estas funciones en Excel 2007 que usan tipos de datos **XLOPER12**. Con la excepción de **xlAutoFree12**, que a veces tendrás que implementar para evitar pérdidas de memoria de **XLOPER12**, puedes omitir sin problemas todas las funciones de la versión 12 **xlAuto**, en cuyo caso, a partir de Excel 2007, Excel llama a las versiones de **XLOPER**. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel llama a la función [xlAutoOpen](xlautoopen.md) cuando se activa el archivo XLL. El complemento se activará al comienzo de una sesión de Excel si estaba activo en la última sesión de Excel que finalizó normalmente. El complemento está activado si se carga durante una sesión de Excel. El complemento puede desactivarse y reactivarse durante una sesión de Excel y se llama a la función durante la reactivación. 
  
Debes usar **xlAutoOpen** para registrar los comandos y funciones de XLL, inicializar estructuras de datos, personalizar la interfaz de usuario, etc. 
  
Si el complemento implementa y exporta la función [xlAutoRegister](xlautoregister-xlautoregister12.md) o la función [xlAutoRegister12](xlautoregister-xlautoregister12.md), Excel puede intentar activar y registrar un comando o función sin llamar primero a la función **xlAutoOpen**. En este caso, debes asegurarte de que la inicialización de tu complemento es suficiente para que tu función o comando funcionen correctamente. Si no es así, debes fracasar en el intento de registrar la función o el comando o llevar a cabo la inicialización necesaria. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel llama a la función [xlAutoClose](xlautoclose.md) cada vez que se desactiva XLL. El complemento se desactivará cuando finalice una sesión de Excel normal. Si el usuario desactiva el complemento durante una sesión de Excel, se llama a la función. 
  
Debes usar **xlAutoClose** para eliminar el registro de comandos y funciones, liberar recursos, deshacer las personalizaciones, etc. 
  
> [!NOTE]
> Hay un problema conocido con la anulación del registro de comandos y funciones. Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel llama a la [función xlAutoAdd](xlautoadd.md) cada vez que el usuario activa el XLL durante una sesión de Excel, mediante el administrador de complementos. No se llama a esta función cuando Excel inicia y carga un complemento preinstalado. 
  
Puedes usar esta función para mostrar el cuadro de diálogo personalizado que indica al usuario que se activó el complemento, para leer o escribir en el registro o para revisar la información de licencias.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel llama a la función [xlAutoRemove](xlautoremove.md) cada vez que el usuario desactiva el XLL durante una sesión de Excel, usando el administrador de complementos. No se llama a esta función cuando una sesión de Excel se cierra, de forma normal o excepcional, con el complemento instalado. 
  
Puedes usar esta función para mostrar el cuadro de diálogo personalizado que indica al usuario que se activó el complemento, o para leer o escribir en el registro.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel llama a la función [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) cuando se invoca al administrador de complementos por primera vez en una sesión de Excel. Si Excel pasa un argumento igual a 1, esta función debe devolver una cadena (normalmente, el nombre del complemento); en caso contrario, debe devolver **#VALUE!**.
  
A partir de Excel 2007, Excel prefiere llamar a la función **xlAddInManagerInfo12** antes que a la función **xlAddInManagerInfo** si lo exporta el XLL. La función **xlAddInManagerInfo12** debe funcionar de la misma forma que la función **xlAddInManagerInfo** para evitar diferencias específicas de la versión en el comportamiento del XLL. La función **xlAddInManagerInfo12** debe devolver un tipo de datos **XLOPER12**, mientras que la función **xlAddInManagerInfo** debe devolver un tipo de datos **XLOPER**. 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel llama a la función [xlAutoRegister](xlautoregister-xlautoregister12.md) cada vez que se realiza una llamada a la función **REGISTRAR** de XML, o a la función de API de C equivalente [xlfRegister](xlfregister-form-1.md), con tipos de devolución y argumentos faltantes para la función que se registra. La función **xlAutoRegister** permite que el XLL busque en sus listas internas de funciones exportadas y comandos para registrar la función con el argumento y devolver los tipos especificados. 
  
A partir de Excel 2007, Excel prefiere llamar a la función **xlAddInRegister12** antes que a la función **xlAddInRegister** si lo exporta el XLL. 
  
> [!NOTE]
> Si **xlAddInRegister**/ **xlAddInRegister12** intenta registrar la función sin proporcionar los tipos de argumento y devoluciones, se produce un bucle de llamada recursiva que eventualmente desborda la pila de llamadas y hace que Excel se cierre o deje de responder. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel llama a la función [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) justo después de que una función de hoja de cálculo de XLL devuelve un tipo de datos **XLOPER**/ **XLOPER12** con una advertencia que le indica a Excel que todavía queda memoria que debe liberarse. Esto permite al XLL devolver matrices, cadenas y referencias externas asignadas dinámicamente a la hoja de cálculo sin pérdidas de memoria. A partir de Excel 2007, se admite el tipo de datos **XLOPER12**. Para obtener más información, consulta [Administración de memoria en Excel](memory-management-in-excel.md).
  
> [!NOTE]
> A partir de Excel 2007, cuando Excel está configurado para usar los nuevos cálculos multiproceso de la hoja de cálculo, se llama a la función **xlAutoFree**/ **xlAutoFree12** en el mismo subproceso que se acaba de usar para llamar a la función que lo devolvió. La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que las celdas de la hoja de cálculo siguientes se evalúen en dicho subproceso. Esto simplifica el diseño de subprocesos seguros en tu XLL. Para obtener más información, consulta [nuevos cálculos multiproceso en Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Crear XLL de 64 bits

Excel y las funciones definidas por el usuario pueden ejecutarse en sistemas operativos de 64 bits para aprovechar las ventajas de desempeño sobre los sistemas operativos de 32 bits. Excel pasa valores en estructuras **XLOPER12** que incluyen información sobre los tipos de datos. Ten cuidado al convertir valores en la estructura **XLOPER12** y los tipos nativos como **int** o punteros para preservar los valores en el tipo más grande. 
  
## <a name="see-also"></a>Ver también



[Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)
  
[Desarrollo de XLL de Excel](developing-excel-xlls.md)

