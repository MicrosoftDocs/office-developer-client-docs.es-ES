---
title: Crear aplicaciones MAPI en plataformas de 32 y 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: 'Última modificación: 09 de marzo de 2015'
localization_priority: Priority
ms.openlocfilehash: 74f321d2c6c8b5159191d4dcdb62e0db21132435
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700419"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Crear aplicaciones MAPI en plataformas de 32 y 64 bits

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
El tema describe las acciones que los desarrolladores de MAPI deben realizar para modificar y volver a crear aplicaciones MAPI de 32 bits para que se ejecuten en una plataforma de 64 bits y aplicaciones de 64 bits para que se ejecuten en una plataforma de 32 bits. En este tema, una plataforma de 64 bits es un equipo con Microsoft Outlook de 64 bits y Windows de 64 bits, y una plataforma de 32 bits es un equipo con un Outlook de 32 bits y Windows de 32 bits o 64 bits. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Sistema operativo y compatibilidad de Office para Outlook de 64 bits

> [!NOTE]
> El término valor de bits se refiere a la distinción entre arquitecturas de procesador de 32 bits y 64 bits, y la compatibilidad de aplicaciones asociada. En este tema, se usa el valor de bits para calificar la versión de Windows, Microsoft Office, Outlook o una aplicación MAPI creada para una arquitectura de procesador de 32 bits o 64 bits de un equipo, y posiblemente otras aplicaciones que se ejecutan en el mismo. 
  
A partir de Microsoft Office 2010, Outlook está disponible como una aplicación de 32 bits y de 64 bits. En el mismo equipo, el valor de bits de Outlook depende del valor de bits del sistema operativo Windows (x86 o x64) y de Microsoft Office, si Office ya está instalado en el equipo. Algunos de los factores que determinan la viabilidad para instalar una versión de 32 bits o de 64 bits de Outlook son:
  
- Office de 32 bits (y Outlook de 32 bits) pueden instalarse en una versión de 32 bits o 64 bits del sistema operativo Windows. Office de 64 bits (y Outlook de 64 bits) pueden instalarse solo en un sistema operativo de 64 bits.
    
- La instalación predeterminada de Office en una versión de 64 bits del sistema operativo Windows es Office de 32 bits.
    
- El valor de bits de una versión instalada de Outlook es siempre el mismo que el valor de bits de Office, si este está instalado en el mismo equipo. Es decir, no se puede instalar una versión de 32 bits de Outlook en el mismo equipo que ya tiene las versiones de 64 bits de otras aplicaciones de Office, como Microsoft Word de 64 bits o Microsoft Excel de 64 bits. De forma similar, no se puede instalar una versión de 64 bits de Outlook en el mismo equipo en el que hay versiones de 32 bits de otras aplicaciones de Office ya instaladas.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Preparar aplicaciones MAPI en plataformas de 32 y 64 bits

Las aplicaciones MAPI incluyen aplicaciones independientes como Microsoft Communicator y MFCMAPI, y proveedores de servicios como proveedores de libreta de direcciones, almacén y transporte. Para que las llamadas a métodos y funciones MAPI funcionen en una aplicación MAPI (excepto una función MAPI simple, MAPISendMail), el valor de bits de la aplicación MAPI debe ser igual al valor de bits del subsistema MAPI del equipo en el que está previsto que se use la aplicación. A su vez, el valor de bits del subsistema MAPI es siempre el mismo y está determinado por el valor de bits de la versión de Outlook instalada. La siguiente tabla resume las acciones necesarias para preparar las aplicaciones MAPI para que se ejecuten en los equipos de destino configurados con Office y Windows con un valor de bits diferente.
  
|Valor de bits de una aplicación MAPI|Valor de bits de Outlook en el equipo de destino|Valor de bits de Windows en el equipo de destino|Acción necesaria para que la aplicación se ejecute en el equipo de destino|
|:-----|:-----|:-----|:-----|
|32 bits  <br/> |32 bits  <br/> |32 o 64 bits  <br/> |No es necesaria ninguna acción.  <br/> |
|32 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Vuelva a crear la aplicación como una aplicación de 64 bits. En caso contrario, todas las llamadas a métodos y funciones MAPI (excepto **MAPISendMail**) producirán un error.  <br/> |
|64 bits  <br/> |64 bits  <br/> |64 bits  <br/> |No es necesaria ninguna acción.  <br/> |
|64 bits  <br/> |32 bits  <br/> |32 o 64 bits  <br/> |Vuelva a crear la aplicación como una aplicación de 32 bits. En caso contrario, todas las llamadas a métodos y funciones MAPI (excepto **MAPISendMail**) producirán un error.  <br/> |
   
Las siguientes secciones explican con más detalle cada escenario. Para los escenarios que requieren volver a crear la aplicación MAPI, vea [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md) para obtener más información sobre el vínculo y la llamada a las funciones MAPI. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>Aplicaciones MAPI de 32 bits y Outlook de 32 bits

Las aplicaciones MAPI compiladas para un subsistema MAPI de 32 bits que está disponible en versiones de 32 bits de Outlook, incluidas las versiones anteriores de Microsoft Outlook 2013, siguen siendo compatibles en equipos con Outlook de 32 bits y sistema operativo Windows de 32 bits o 64 bits. No hay ninguna acción específica necesaria para los desarrolladores de la aplicación.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>Aplicaciones MAPI de 32 bits y Outlook de 64 bits

Las aplicaciones MAPI de 32 bits no se pueden ejecutar en un equipo con Outlook de 64 bits y Windows de 64 bits. El desarrollador de la aplicación tendrá que actualizar y volver a crear la aplicación como una aplicación de 64 bits para la plataforma de 64 bits. Esto ocurre porque una aplicación de 32 bits no puede cargar un archivo Msmapi32.dll de 64 bits. Hay un pequeño número de cambios en la API que deben incorporar los desarrolladores de la aplicación para compilar el código correctamente en un entorno de 64 bits. Los archivos de encabezado MAPI se han actualizado con estos cambios para admitir la plataforma de 64 bits. Puede descargar estos archivos de encabezado en [Outlook 2010: archivos de encabezado MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Los desarrolladores pueden usar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones MAPI de 32 bits y 64 bits.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>Aplicaciones MAPI de 64 bits y Outlook de 64 bits

Las aplicaciones MAPI de 64 bits se pueden ejecutar en un equipo con Outlook de 64 bits y Windows de 64 bits. No hay ninguna acción específica necesaria para los desarrolladores de la aplicación.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>Aplicaciones MAPI de 64 bits y Outlook de 32 bits

Las aplicaciones MAPI de 64 bits no se pueden ejecutar en un equipo con Outlook de 32 bits y Windows de 32 o 64 bits. El desarrollador de la aplicación tendrá que actualizar y volver a crear la aplicación como una aplicación de 32 bits para que funcione con Outlook de 32 bits. Use los archivos de encabezado MAPI actualizados, que puede descargar en [Outlook 2010: archivos de encabezado MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Los desarrolladores pueden usar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones MAPI de 32 bits y 64 bits.
  
### <a name="exception-mapisendmail"></a>Excepción: MAPISendMail

En general, una aplicación MAPI de 32 bits no debe ejecutarse en una plataforma de 64 bits (Outlook de 64 bits en Windows de 64 bits), sin la necesidad de volver a crearla como una aplicación de 64 bits, y una aplicación MAPI de 64 bits no debe ejecutarse en un equipo con Outlook de 32 bits y Windows de 32 bits o 64 bits, sin la necesidad de volver a crearla como una aplicación de 32 bits. La figura 1 muestra un cuadro de diálogo de alerta que aparece si se produce cualquiera de estos escenarios.
  
**Figura 1. Mensaje de error para la mayoría de las llamadas MAPI de bits cruzados**

![Mensaje de error para la mayoría de las llamadas MAPI de bits cruzados](media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Mensaje de error para la mayoría de las llamadas MAPI de bits cruzados")
  
Pero una llamada de función entre todos los elementos de MAPI simple y MAPI, **MAPISendMail**, funciona correctamente en un escenario de Windows-32-bit-on-Windows-64-bit (WOW64) o Windows-64-bit-on-Windows-32-bit (WOW32) y no produciría la alerta anterior. Este escenario WOW64 solo se aplica a Windows 7. 

La figura 2 muestra un escenario de WOW64 en el que una aplicación MAPI de 32 bits llama a **MAPISendMail** en un equipo con Windows 7 de 64 bits. En este escenario, la biblioteca MAPI realiza una llamada COM para iniciar una aplicación Fixmapi de 64 bits. La aplicación Fixmapi implícitamente se vincula a la biblioteca MAPI, que dirige la llamada de función al código auxiliar MAPI de Windows, que a su vez reenvía la llamada al código auxiliar MAPI de Outlook, lo que permite que la llamada de función **MAPISendMail** funcione correctamente. 
  
**Figura 2. Procesar MAPISendMail en un escenario de WOW64.**

![Procesar MAPISendMail en un escenario de WOW64](media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Procesar MAPISendMail en un escenario de WOW64")
  
## <a name="see-also"></a>Vea también

- [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md)

