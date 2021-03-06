---
title: Programar con la API de C en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d07217fe410fedb18da4600ab07078d1aaf5d083
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310470"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programar con la API de C en Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Puede usar el Microsoft Excel 2013 Kit de desarrollo de software de XLL y la API de C para crear funciones de hoja de cálculo de alto rendimiento para Excel 2013. Las actualizaciones para la Excel 2013API de C reflejan compatibilidad continua para los usuarios para los que es fundamental el rendimiento de la funcionalidad de manera interna o de terceros.
  
## <a name="excel-programming-interfaces"></a>Interfaces de programación de Excel

Excel proporciona varias opciones para desarrollar aplicaciones que se comunican con él. Las interfaces de programación de Excel se han agregado a las versiones anteriores en el orden siguiente:
  
- **Lenguaje de macros XLM:** el primer lenguaje al que pueden acceder los usuarios de la extensión de Excel y la base de la API de C. Aunque todavía se admite en Excel 2010, Visual Basic para aplicaciones (VBA) ha reemplazado durante mucho tiempo a XML. 
    
- **API de C y XLL:** DLL integrados con Excel. Estos DLL proporcionan interfaz más directa y rápida para agregar funciones de hoja de cálculo de alto rendimiento, aunque a costa de una cierta complejidad en comparación con las tecnologías posteriores. 
    
- **VBA:** objetos de código de Visual Basic asociados a objetos de libro de Excel. VBA permite la captura de eventos, la personalización y la adición de comandos y funciones definidas por el usuario. VBA es la opción de extensibilidad más usada y más fácilmente disponible. 
    
- **COM:** el estándar de interoperabilidad para aplicaciones basadas en Windows, a través del cual Excel expone sus eventos y objetos. VBA utiliza COM para interactuar con Excel. Excel exporta bibliotecas de tipos COM que pueden ayudarle a crear aplicaciones y recursos de código de C++ COM que se pueden controlar Excel externamente. 
    
- **Microsoft .NET Framework:** el entorno de código administrado multilenguaje diseñado para el desarrollo rápido de aplicaciones para entornos distribuidos. El lenguaje de programación primario para el código que se basa en .NET Framework es C#, aunque muchos lenguajes se pueden compilar en el lenguaje intermedio de Microsoft (MSIL). Excel 2013 puede acceder a recursos de código dentro de los ensamblados de .NET Framework. 
    
## <a name="when-to-use-the-c-api"></a>Cuándo usar la API de C

El motivo principal para escribir XLL y usar la API de C es crear funciones de hoja de cálculo de alto rendimiento. Aunque las funciones XLL se conocen frecuentemente como funciones definidas por el usuario, la inversión de tiempo para obtener el conocimiento y las habilidades necesarias para escribir XLL hacen que esta tecnología no sea práctica para la mayoría de los usuarios. Sin embargo, las aplicaciones de funciones de alto rendimiento y, en Excel 2013, la capacidad para escribir interfaces multiproceso en recursos de servidor potentes, hacen que sea una parte muy importante de la extensibilidad de Excel. 
  
La revisión de la API de C que se introdujo en Excel 2007 principalmente se ocupa de los aspectos relativos a los cálculos de alto rendimiento, en lugar de características como la interfaz de usuario.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Escribir funciones de hoja de cálculo de alto rendimiento definidas por el usuario

La API de C de Excel es la opción ideal cuando quiera crear funciones de hoja de cálculo de alto rendimiento con complementos XLL. La API de C proporciona el acceso más directo a los datos de hoja de cálculo. XLL proporciona a Excel el acceso más directo a los recursos DLL. Se ha mejorado aún más el rendimiento de XLL en Excel 2013 mediante la adición de nuevos tipos de datos y, más importante, compatibilidad para ejecutar funciones definidas por el usuario en los servidores en clúster.
  
Trabajar con los XLL tiene un costo: la API C no tiene ninguna de las características de desarrollo rápido de nivel superior de VBA, COM o .NET Framework. La administración de memoria es de bajo nivel y, por lo tanto, da mayor responsabilidad al desarrollador. Muchas características de Excel expuestas a través de COM, para que estén disponibles a través de VBA y .NET Framework, no están expuestas a la API de C.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Acceder a servidores multiproceso con las funciones de hoja de cálculo XLL

La actualización multiproceso (MTR), que se introdujo en Excel 2007, permite crear funciones de hoja de cálculo XLL de subprocesos. Puede usar estas funciones para acceder a servidores multiproceso. Las secciones posteriores describen con más detalle cómo esto puede aumentar significativamente el rendimiento observado por el usuario. Para los usuarios de Excel que a veces necesitan acceder a una gran cantidad de capacidad de procesamiento, la combinación de un XLL que usa MTR y un servidor de cálculo eficaz ofrece la solución de mayor rendimiento.
  
### <a name="customizing-the-excel-user-interface"></a>Personalizar la interfaz de usuario de Excel

En muchas versiones de Excel, la API de C no es la mejor opción para personalizar la interfaz de usuario. VBA tiene un mejor acceso a los objetos y eventos de Excel. La interfaz de usuario que se introdujo en Excel 2007 es significativamente diferente de las versiones anteriores en apariencia y en la tecnología subyacente. Puede personalizar esta interfaz con recursos de código administrado.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Crear aplicaciones a las que puede acceder en Internet

Los servicios de Excel que se introdujeron con el sistema Microsoft Office 2007, proporcionan la mejor manera de proporcionar acceso a los usuarios a los libros y a la funcionalidad de Excel con herramientas estándar de explorador web. Junto con los lenguajes de desarrollo .NET Framework y los recursos, estas tecnologías representan una parte importante de la implementación de Excel para los usuarios en el futuro.
  
### <a name="controlling-excel-from-external-applications"></a>Controlar Excel desde aplicaciones externas

Excel expone sus objetos, métodos y eventos a través de la interfaz COM. Por lo tanto, puede usar COM para crear aplicaciones independientes que pueden iniciar y controlar una sesión de Excel o controlar una sesión de Excel existente. Puede acceder a la interfaz de Excel expuesta a COM dentro de varios lenguajes de desarrollo, incluidos C++ y VBA. De forma parecida, C# y .NET Framework proporcionan una interfaz para Excel que permite el acceso remoto y el control de Excel.
  
## <a name="asynchronous-calling-of-excel"></a>Llamada asincrónica de Excel

Excel permite que los XLL llamen a la API de C solo cuando Excel pasa el control al XLL. Una función de hoja de cálculo a la que llama Excel puede devolver la llamada a Excel con la API de C. Un comando XLL al que llama Excel puede llamar a la API de C. Las funciones y los comandos DLL y XLL a los que llama VBA cuando Excel ha llamado a VBA, pueden llamar a la API de C. Por ejemplo, no puede configurar una devolución de llamada con hora de Windows en el XLL y llamar a la API de C desde él, y no puede llamar a la API de C desde un subproceso en segundo plano creado por el XLL. No se recomienda la llamada asincrónica a Excel con COM desde un DLL o XLL.
  
Esto es muy restrictivo porque puede haber aplicaciones en el que quiera que Excel reaccione a un evento de forma asincrónica. Por ejemplo, es posible que quiera que Excel recupere una parte de los datos de Internet y vuelva a calcular cada vez que se cambien los datos. O bien, puede que quiera que un subproceso en segundo plano realice un cálculo y hacer que Excel vuelva a calcular cuando termine.
  
Puede hacerlo haciendo que Excel sondee activamente los cambios, pero no resulta muy eficaz y limita porque, con frecuencia, implica la interrupción de la actividad normal de Excel. Puede configurar comandos programados repetidos con la API de C o VBA, aunque no es una solución ideal.
  
Idealmente, quiere un proceso externo más eficaz para comprobar los cambios en los datos y para que el proceso externo desencadene Excel para recuperar la actualización y volver a realizar un cálculo. Puede hacerlo con una aplicación que se comunique con Excel mediante COM. COM no está restringido de la misma manera que la API de C para realizar llamadas solo cuando Excel pase explícitamente control. Las aplicaciones COM pueden invocar métodos de Excel siempre que Excel esté en estado preparado, aunque estas llamadas al método se pueden omitir si se muestran cuadros de diálogo, se extraen los menús o cuando se ejecuta una macro.
  
## <a name="c-api-and-its-relation-to-xlm"></a>API de C y su relación con XLM

El lenguaje de macros (XLM) de Excel fue el primer entorno de programación accesible para los usuarios que se proporcionó en Excel. Habilitó a los usuarios para crear comandos y funciones personalizados de hojas de macros especiales que se parecen a las hojas de cálculo normales. Las hojas de macro XLM todavía se admiten en Excel 2013. Puede usar todas las funciones de hoja de cálculo habituales, como **SUM** y **LOG**, en una hoja de macros además de los siguientes elementos que no se pueden introducir en una hoja de cálculo: 
  
- Información de las funciones del área de trabajo, **GET.CELL** y **GET.WORKBOOK**.
    
- Funciones equivalentes a comandos que permiten la automatización de las operaciones de usuario normales, como **DEFINE.NAME** y **PASTE**.
    
- Funciones relacionadas con complementos, como **REGISTER**.
    
- Capturas de eventos equivalentes a comandos, como **ON.ENRTY** y **ON.TIME**.
    
- Operaciones específicas de funciones de macro, como **ARGUMENT** y **VOLATILE**.
    
- Operaciones de control de flujo, como **GOTO** y **RETURN**.
    
Una versión limitada de la API de C existía en la versión 3 de Excel. Sin embargo, en Excel versión 4, el lenguaje XLM se asigna a la API de C. Desde entonces, los DLL han podido llamar a todas las funciones de hoja de cálculos, funciones de información de hoja de macros y comandos, y para configurar capturas de eventos. Los DLL no pueden llamar a las funciones de control de flujo XLM desde dentro de la API de C. Estas funciones de hoja de macros y comandos están documentados en el archivo Ayuda XLMacr8.hlp (anteriormente denominado Macrofun.hlp). Para obtener este archivo de ayuda, vaya al [Centro de descarga de Microsoft](https://download.microsoft.com) y busque "XLMacr8.hlp". 
  
> [!NOTE]
> Windows Vista y Windows 7 no admiten directamente los archivos .hlp, pero puede descargar el [programa Ayuda de Windows (WinHlp32.exe) para Windows Vista](https://go.microsoft.com/fwlink/?LinkID=82148) o el [programa Ayuda de Windows (WinHlp32.exe) para Windows 7](https://www.microsoft.com/download/en/details.aspx?id=91) de Microsoft, que permite que se abran. 
  
Los DLL llaman a los equivalentes de la API de C de estas funciones y comandos con las funciones de devolución de llamada **Excel4**, **Excel4v**, **Excel12** y **Excel12v** (las dos últimas se introdujeron en Excel 2007). Las constantes enumeradas que se corresponden a cada función y el comando se definen en un archivo de encabezado y se pasan como uno de estos argumentos para estas devoluciones de llamada. Por ejemplo, **GET.CELL** está representado por **xlfGetCell**, **REGISTER** por **xlfRegister** y **DEFINE.NAME** por **xlcDefineName**.
  
Además de proporcionar las funciones de hoja de cálculo, las funciones de hoja de macros y los comandos, la API de C proporciona enumeraciones de función y de comando a las que se puede llamar con estas devoluciones de llamada desde un DLL. Por ejemplo, **xlGetName** habilita el DLL averiguar su propio nombre de archivo y ruta de acceso completa, que son necesarios al registrar funciones y comandos con Excel. 
  
Desde la introducción de las hojas de Visual Basic para aplicaciones (VBA) en la versión 5 de Excel y el Editor de Visual Basic (VBE) en la versión 8 (Excel 97), la forma más sencilla para los usuarios de personalizar Excel es usar VBA en lugar de XLM. Por lo tanto, muchas de las nuevas funcionalidades introducidas en versiones posteriores de Excel están disponibles a través de VBA, pero no a través de XLM o la API de C. Por ejemplo, están disponibles varios comandos, capturas de eventos y capacidades de cuadro de diálogo mejoradas a través de VBA, pero no a través de XLM o de la API de C.
  
Para más información, consulte [Novedades de la API C para Excel 2013](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Vea también



[Novedades de la API de C para Excel](what-s-new-in-the-c-api-for-excel.md)
  
[Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Introducción al SDK de XLL de Excel](getting-started-with-the-excel-xll-sdk.md)

