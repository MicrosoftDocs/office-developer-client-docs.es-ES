---
title: Programar con la API de C en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815693"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programar con la API de C en Excel

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Puede usar el Microsoft Excel 2013 Kit de desarrollo de software de XLL y la API de C para crear funciones de hoja de c�lculo de alto rendimiento para Excel 2013. Las actualizaciones para la Excel 2013API de C reflejan compatibilidad continua para los usuarios para los que es fundamental el rendimiento de la funcionalidad de manera interna o de terceros.
  
## <a name="excel-programming-interfaces"></a>Interfaces de programaci�n de Excel

Excel proporciona varias opciones para desarrollar aplicaciones que se comunican con �l. Las interfaces de programaci�n de Excel se han agregado a las versiones anteriores en el orden siguiente:
  
- **Lenguaje de macros XLM:** el primer lenguaje al que pueden acceder los usuarios de la extensi�n de Excel y la base de la API de C. Aunque todav�a se admite en Excel 2010, Visual Basic para aplicaciones (VBA) ha reemplazado durante mucho tiempo a XML. 
    
- **API de C y XLL:** DLL integrados con Excel. Estos DLL proporcionan interfaz m�s directa y r�pida para agregar funciones de hoja de c�lculo de alto rendimiento, aunque a costa de una cierta complejidad en comparaci�n con las tecnolog�as posteriores. 
    
- **VBA:** objetos de c�digo de Visual Basic asociados a objetos de libro de Excel. VBA permite la captura de eventos, la personalizaci�n y la adici�n de comandos y funciones definidas por el usuario. VBA es la opci�n de extensibilidad m�s usada y m�s f�cilmente disponible. 
    
- **COM:** el est�ndar de interoperabilidad para aplicaciones basadas en Windows, a trav�s del cual Excel expone sus eventos y objetos. VBA utiliza COM para interactuar con Excel. Excel exporta bibliotecas de tipos COM que pueden ayudarle a crear aplicaciones y recursos de c�digo de C++ COM que se pueden controlar Excel externamente. 
    
- **Microsoft .NET Framework:** el entorno de c�digo administrado multilenguaje dise�ado para el desarrollo r�pido de aplicaciones para entornos distribuidos. El lenguaje de programaci�n primario para el c�digo que se basa en .NET Framework es C#, aunque muchos lenguajes se pueden compilar en el lenguaje intermedio de Microsoft (MSIL). Excel 2013 puede acceder a recursos de c�digo dentro de los ensamblados de .NET Framework. 
    
## <a name="when-to-use-the-c-api"></a>Cu�ndo usar la API de C

El motivo principal para escribir XLL y usar la API de C es crear funciones de hoja de c�lculo de alto rendimiento. Aunque las funciones XLL se conocen frecuentemente como funciones definidas por el usuario, la inversi�n de tiempo para obtener el conocimiento y las habilidades necesarias para escribir XLL hacen que esta tecnolog�a no sea pr�ctica para la mayor�a de los usuarios. Sin embargo, las aplicaciones de funciones de alto rendimiento y, en Excel 2013, la capacidad para escribir interfaces multiproceso en recursos de servidor potentes, hacen que sea una parte muy importante de la extensibilidad de Excel. 
  
La revisi�n de la API de C que se introdujo en Excel 2007 principalmente se ocupa de los aspectos relativos a los c�lculos de alto rendimiento, en lugar de caracter�sticas como la interfaz de usuario.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Escribir funciones de hoja de c�lculo de alto rendimiento definidas por el usuario

La API de C de Excel es la opci�n ideal cuando quiera crear funciones de hoja de c�lculo de alto rendimiento con complementos XLL. La API de C proporciona el acceso m�s directo a los datos de hoja de c�lculo. XLL proporciona a Excel el acceso m�s directo a los recursos DLL. Se ha mejorado a�n m�s el rendimiento de XLL en Excel 2013 mediante la adici�n de nuevos tipos de datos y, m�s importante, compatibilidad para ejecutar funciones definidas por el usuario en los servidores en cl�ster.
  
Trabajar con los XLL tiene un costo: la API C no tiene ninguna de las caracter�sticas de desarrollo r�pido de nivel superior de VBA, COM o .NET Framework. La administraci�n de memoria es de bajo nivel y, por lo tanto, da mayor responsabilidad al desarrollador. Muchas caracter�sticas de Excel expuestas a trav�s de COM, para que est�n disponibles a trav�s de VBA y .NET Framework, no est�n expuestas a la API de C.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Acceder a servidores multiproceso con las funciones de hoja de c�lculo XLL

La actualizaci�n multiproceso (MTR), que se introdujo en Excel 2007, permite crear funciones de hoja de c�lculo XLL de subprocesos. Puede usar estas funciones para acceder a servidores multiproceso. Las secciones posteriores describen con m�s detalle c�mo esto puede aumentar significativamente el rendimiento observado por el usuario. Para los usuarios de Excel que a veces necesitan acceder a una gran cantidad de capacidad de procesamiento, la combinaci�n de un XLL que usa MTR y un servidor de c�lculo eficaz ofrece la soluci�n de mayor rendimiento.
  
### <a name="customizing-the-excel-user-interface"></a>Personalizar la interfaz de usuario de Excel

En muchas versiones de Excel, la API de C no es la mejor opci�n para personalizar la interfaz de usuario. VBA tiene un mejor acceso a los objetos y eventos de Excel. La interfaz de usuario que se introdujo en Excel 2007 es significativamente diferente de las versiones anteriores en apariencia y en la tecnolog�a subyacente. Puede personalizar esta interfaz con recursos de c�digo administrado.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Crear aplicaciones a las que puede acceder en Internet

Los servicios de Excel que se introdujeron con el sistema Microsoft Office 2007, proporcionan la mejor manera de proporcionar acceso a los usuarios a los libros y a la funcionalidad de Excel con herramientas est�ndar de explorador web. Junto con los lenguajes de desarrollo .NET Framework y los recursos, estas tecnolog�as representan una parte importante de la implementaci�n de Excel para los usuarios en el futuro.
  
### <a name="controlling-excel-from-external-applications"></a>Controlar Excel desde aplicaciones externas

Excel expone sus objetos, m�todos y eventos a trav�s de la interfaz COM. Por lo tanto, puede usar COM para crear aplicaciones independientes que pueden iniciar y controlar una sesi�n de Excel o controlar una sesi�n de Excel existente. Puede acceder a la interfaz de Excel expuesta a COM dentro de varios lenguajes de desarrollo, incluidos C++ y VBA. De forma parecida, C# y .NET Framework proporcionan una interfaz para Excel que permite el acceso remoto y el control de Excel.
  
## <a name="asynchronous-calling-of-excel"></a>Llamada asincr�nica de Excel

Excel permite que los XLL llamen a la API de C solo cuando Excel pasa el control al XLL. Una funci�n de hoja de c�lculo a la que llama Excel puede devolver la llamada a Excel con la API de C. Un comando XLL al que llama Excel puede llamar a la API de C. Las funciones y los comandos DLL y XLL a los que llama VBA cuando Excel ha llamado a VBA, pueden llamar a la API de C. Por ejemplo, no puede configurar una devoluci�n de llamada con hora de Windows en el XLL y llamar a la API de C desde �l, y no puede llamar a la API de C desde un subproceso en segundo plano creado por el XLL. No se recomienda la llamada asincr�nica a Excel con COM desde un DLL o XLL.
  
Esto es muy restrictivo porque puede haber aplicaciones en el que quiera que Excel reaccione a un evento de forma asincr�nica. Por ejemplo, es posible que quiera que Excel recupere una parte de los datos de Internet y vuelva a calcular cada vez que se cambien los datos. O bien, puede que quiera que un subproceso en segundo plano realice un c�lculo y hacer que Excel vuelva a calcular cuando termine.
  
Puede hacerlo haciendo que Excel sondee activamente los cambios, pero no resulta muy eficaz y limita porque, con frecuencia, implica la interrupci�n de la actividad normal de Excel. Puede configurar comandos programados repetidos con la API de C o VBA, aunque no es una soluci�n ideal.
  
Idealmente, quiere un proceso externo m�s eficaz para comprobar los cambios en los datos y para que el proceso externo desencadene Excel para recuperar la actualizaci�n y volver a realizar un c�lculo. Puede hacerlo con una aplicaci�n que se comunique con Excel mediante COM. COM no est� restringido de la misma manera que la API de C para realizar llamadas solo cuando Excel pase expl�citamente control. Las aplicaciones COM pueden invocar m�todos de Excel siempre que Excel est� en estado preparado, aunque estas llamadas al m�todo se pueden omitir si se muestran cuadros de di�logo, se extraen los men�s o cuando se ejecuta una macro.
  
## <a name="c-api-and-its-relation-to-xlm"></a>API de C y su relaci�n con XLM

El lenguaje de macros (XLM) de Excel fue el primer entorno de programaci�n accesible para los usuarios que se proporcion� en Excel. Habilit� a los usuarios para crear comandos y funciones personalizados de hojas de macros especiales que se parecen a las hojas de c�lculo normales. Las hojas de macro XLM todav�a se admiten en Excel 2013. Puede usar todas las funciones de hoja de c�lculo habituales, como **SUM** y **LOG**, en una hoja de macros adem�s de los siguientes elementos que no se pueden introducir en una hoja de c�lculo: 
  
- Informaci�n de las funciones del �rea de trabajo, **GET.CELL** y **GET.WORKBOOK**.
    
- Funciones equivalentes a comandos que permiten la automatizaci�n de las operaciones de usuario normales, como **DEFINE.NAME** y **PASTE**.
    
- Funciones relacionadas con complementos, como **REGISTER**.
    
- Capturas de eventos equivalentes a comandos, como **ON.ENRTY** y **ON.TIME**.
    
- Operaciones espec�ficas de funciones de macro, como **ARGUMENT** y **VOLATILE**.
    
- Operaciones de control de flujo, como **GOTO** y **RETURN**.
    
Una versi�n limitada de la API de C exist�a en la versi�n 3 de Excel. Sin embargo, en Excel versi�n 4, el lenguaje XLM se asigna a la API de C. Desde entonces, los DLL han podido llamar a todas las funciones de hoja de c�lculos, funciones de informaci�n de hoja de macros y comandos, y para configurar capturas de eventos. Los DLL no pueden llamar a las funciones de control de flujo XLM desde dentro de la API de C. Estas funciones de hoja de macros y comandos est�n documentados en el archivo Ayuda XLMacr8.hlp (anteriormente denominado Macrofun.hlp). Para obtener este archivo de ayuda, vaya al [Centro de descarga de Microsoft](http://download.microsoft.com) y busque "XLMacr8.hlp". 
  
> [!NOTE]
> [!NOTA] Windows Vista y Windows 7 no admiten directamente los archivos .hlp, pero puede descargar el [programa Ayuda de Windows (WinHlp32.exe) para Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) o el [programa Ayuda de Windows (WinHlp32.exe) para Windows 7](http://www.microsoft.com/download/en/details.aspx?id=91) de Microsoft, que permite que se abran. 
  
Los DLL llaman a los equivalentes de la API de C de estas funciones y comandos con las funciones de devoluci�n de llamada **Excel4**, **Excel4v**, **Excel12** y **Excel12v** (las dos �ltimas se introdujeron en Excel 2007). Las constantes enumeradas que se corresponden a cada funci�n y el comando se definen en un archivo de encabezado y se pasan como uno de estos argumentos para estas devoluciones de llamada. Por ejemplo, **GET.CELL** est� representado por **xlfGetCell**, **REGISTER** por **xlfRegister** y **DEFINE.NAME** por **xlcDefineName**.
  
Adem�s de proporcionar las funciones de hoja de c�lculo, las funciones de hoja de macros y los comandos, la API de C proporciona enumeraciones de funci�n y de comando a las que se puede llamar con estas devoluciones de llamada desde un DLL. Por ejemplo, **xlGetName** habilita el DLL averiguar su propio nombre de archivo y ruta de acceso completa, que son necesarios al registrar funciones y comandos con Excel. 
  
Desde la introducci�n de las hojas de Visual Basic para aplicaciones (VBA) en la versi�n 5 de Excel y el Editor de Visual Basic (VBE) en la versi�n 8 (Excel 97), la forma m�s sencilla para los usuarios de personalizar Excel es usar VBA en lugar de XLM. Por lo tanto, muchas de las nuevas funcionalidades introducidas en versiones posteriores de Excel est�n disponibles a trav�s de VBA, pero no a trav�s de XLM o la API de C. Por ejemplo, est�n disponibles varios comandos, capturas de eventos y capacidades de cuadro de di�logo mejoradas a trav�s de VBA, pero no a trav�s de XLM o de la API de C.
  
Para m�s informaci�n, consulte [Novedades de la API C para Excel 2013](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Vea tambi�n



[Novedades de la API C para Excel 2013](what-s-new-in-the-c-api-for-excel.md)
  
[Devoluci�n de llamada de API de C funciona Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Introducci�n al SDK de XLL de Excel 2013](getting-started-with-the-excel-xll-sdk.md)

