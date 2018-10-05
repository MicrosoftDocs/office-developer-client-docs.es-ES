---
title: Creación de aplicaciones MAPI en plataformas de 32 bits y 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bc98b201b31048e22e093d92c9cf2d5ff1fb0257
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383152"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Creación de aplicaciones MAPI en plataformas de 32 bits y 64 bits

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
En este tema se describe las acciones que deberían seguir los desarrolladores MAPI para cambiar y volver a generar las aplicaciones de MAPI de 32 bits se ejecuten en una plataforma de 64 bits y las aplicaciones de 64 bits se ejecuten en una plataforma de 32 bits. En este tema, una plataforma de 64 bits es un equipo que se instala con Windows de 64 bits y de 64 bits de Microsoft Outlook y una plataforma de 32 bits es un equipo que se instala con un Outlook de 32 bits y Windows de 32 bits o 64 bits. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Compatibilidad de Office para Outlook de 64 bits y sistema operativo

> [!NOTE]
> El valor de bits de términos se refiere a la distinción entre las arquitecturas de procesador de 32 bits y 64 bits y la compatibilidad de aplicaciones asociada. En este tema, el valor de bits se utiliza para calificar la versión de Windows, Microsoft Office, Outlook, o una aplicación de MAPI creada para adaptarla a una arquitectura de procesador de 32 bits o 64 bits de un equipo y, posiblemente, otras aplicaciones que se ejecutan en ese equipo. 
  
A partir de Microsoft Office 2010, Outlook está disponible como una aplicación de 64 bits y de 32 bits. En el mismo equipo, el valor de bits de Outlook depende del valor de bits del sistema operativo Windows (x86 o x64) y de Microsoft Office, si Office ya está instalado en el equipo. Los siguientes son algunos de los factores que determinan la viabilidad de la instalación de 32 bits o una versión de 64 bits de Outlook:
  
- Office de 32 bits (y de Outlook de 32 bits) pueden instalarse en una versión de 32 bits o 64 bits del sistema operativo Windows. Office de 64 bits (y Outlook de 64 bits) pueden instalarse solo en un sistema operativo de 64 bits.
    
- La instalación predeterminada de Office en una versión de 64 bits del sistema operativo Windows es Office de 32 bits.
    
- El valor de bits de una versión instalada de Outlook siempre es el mismo que el valor de bits de Office, si Office está instalado en el mismo equipo. En otras palabras, no se puede instalar una versión de 32 bits de Outlook en el mismo equipo que ya tiene las versiones de 64 bits de otras aplicaciones de Office instaladas, como Microsoft Word de 64 bits o 64 bits de Microsoft Excel. De forma similar, no se puede instalar una versión de 64 bits de Outlook en el mismo equipo que ya tiene las versiones de 32 bits de otras aplicaciones de Office instaladas.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Preparación de aplicaciones de MAPI para plataformas de 32 bits y 64 bits

Las aplicaciones MAPI incluyen aplicaciones independientes, como Microsoft Communicator y MFCMAPI y proveedores de servicios como la libreta de direcciones, almacén y los proveedores de transporte. Para la función y método MAPI llamadas para que funcionen en una aplicación de MAPI (a excepción de una función de MAPI Simple, MAPISendMail), el valor de bits de la aplicación MAPI deben ser el mismo que el valor de bits del subsistema MAPI en el equipo que la aplicación está destinada a ejecutar en. El valor de bits del subsistema MAPI, a su vez, se determina por y siempre el mismo que el valor de bits de la versión instalada de Outlook. En la siguiente tabla se resume las acciones necesarias para preparar las aplicaciones de MAPI se ejecuten en equipos de destino configurados con Office y Windows de valor de bits distintos.
  
|Valor de bits de la aplicación de MAPI|Valor de bits de Outlook en el equipo de destino|Valor de bits de Windows en el equipo de destino|Acción necesaria para habilitar la aplicación para que se ejecute en el equipo de destino|
|:-----|:-----|:-----|:-----|
|32-bit  <br/> |32-bit  <br/> |32 bits o 64 bits  <br/> |No es necesaria ninguna acción específica.  <br/> |
|32-bit  <br/> |64 bits  <br/> |64 bits  <br/> |Vuelve a crear la aplicación como una aplicación de 64 bits. De lo contrario, se producirá un error en todas las llamadas de método y función MAPI (excepto **MAPISendMail**).  <br/> |
|64 bits  <br/> |64 bits  <br/> |64 bits  <br/> |No es necesaria ninguna acción específica.  <br/> |
|64 bits  <br/> |32-bit  <br/> |32 bits o 64 bits  <br/> |Vuelve a crear la aplicación como una aplicación de 32 bits. De lo contrario, se producirá un error en todas las llamadas de método y función MAPI (excepto **MAPISendMail**).  <br/> |
   
Aún más las siguientes secciones explican cada escenario. Para los escenarios que requieren volver a generar la aplicación MAPI, vea [Vincular a las funciones de MAPI](how-to-link-to-mapi-functions.md) para obtener información adicional acerca de la vinculación a y llamar a funciones MAPI. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>aplicación de MAPI de 32 bits y de Outlook de 32 bits

Las aplicaciones MAPI compiladas para un subsistema MAPI de 32 bits que está disponible en versiones de 32 bits de Outlook, incluidas las versiones anteriores de Microsoft Outlook 2013, siguen siendo compatibles en equipos instalados con Outlook de 32 bits y un Windows de 32 bits o 64 bits Sistema operativo. No hay ninguna acción específica necesarios para los desarrolladores de aplicaciones.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>aplicación de MAPI de 32 bits y 64 bits Outlook

no se admiten las aplicaciones de MAPI de 32 bits para ejecutar en un equipo que se instala con Outlook de 64 bits y 64 bits de Windows. El desarrollador de aplicaciones debe actualizar y volver a generar la aplicación como una aplicación de 64 bits para la plataforma de 64 bits. Esto es debido a que una aplicación de 32 bits no puede cargar un archivo Msmapi32.dll de 64 bits. Hay un pequeño número de cambios en la API que los desarrolladores de aplicaciones deben incorporar para generar su código correctamente para un entorno de 64 bits. Se han actualizado los archivos de encabezado MAPI con estos cambios para admitir la plataforma de 64 bits. Puede descargar estos archivos de encabezado en [Outlook 2010: archivos de encabezado de MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Los desarrolladores pueden utilizar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones de MAPI de 32 bits y 64 bits.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>aplicación de MAPI de 64 bits y 64 bits Outlook

se admiten las aplicaciones de MAPI de 64 bits en equipos instalados con Outlook de 64 bits y 64 bits de Windows. No hay ninguna acción específica necesarios para los desarrolladores de aplicaciones.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>aplicación de 64 bits MAPI y Outlook de 32 bits

no se admiten las aplicaciones de MAPI de 64 bits para ejecutar en un equipo que se instala con Outlook de 32 bits y Windows de 32 bits o 64 bits. El desarrollador de aplicaciones debe actualizar y volver a generar la aplicación como una aplicación de 32 bits para trabajar con Outlook de 32 bits. Usar los archivos de encabezado MAPI actualizados, que puede descargar en [Outlook 2010: archivos de encabezado de MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Los desarrolladores pueden utilizar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones de MAPI de 32 bits y 64 bits.
  
### <a name="exception-mapisendmail"></a>Excepción: MAPISendMail

En general, no debe ejecutar una aplicación de MAPI de 32 bits de 64 bits plataforma (Outlook de 64 bits en Windows de 64 bits), sin que se va a primera regenerada como una aplicación de 64 bits y una aplicación de 64 bits MAPI no deben ejecutar en un equipo que se instala con Outlook de 32 bits y 32 bits o 64 bits Windows sin primero va a volver a crear como una aplicación de 32 bits. La figura 1 muestra un cuadro de diálogo de alerta que se mostrarían si se produce uno de estos escenarios.
  
**En la figura 1. Se llama el mensaje de error para la mayoría de bits cruzados MAPI.**

![Mensaje de error para las llamadas MAPI más cruzados] (media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Mensaje de error para las llamadas MAPI más cruzados")
  
Sin embargo, una llamada de función entre los elementos de todos los Simple MAPI y MAPI, **MAPISendMail**, realizarían correctamente en un escenario de Windows-64-bit-on-Windows-32-bit (WOW32) o Windows-32-bit-on-Windows-64-bit (WOW64) y no diese como resultado de la alerta anterior. En este escenario de WOW64 sólo se aplica a Windows 7. 

La figura 2 muestra un escenario de WOW64 en el que llama a una aplicación de MAPI de 32 bits **MAPISendMail** en un equipo que se instala con Windows 7 de 64 bits. En este escenario, la biblioteca MAPI realiza una llamada de COM para iniciar una aplicación de 64 bits Fixmapi. La aplicación Fixmapi implícitamente contiene vínculos a la biblioteca MAPI, que enruta la llamada de función al código auxiliar de MAPI de Windows, que a su vez reenvía la llamada a la agrupación de MAPI de Outlook, lo que permite la llamada de función **MAPISendMail** se realice correctamente. 
  
**La figura 2. Procesamiento de MAPISendMail en un escenario de WOW64.**

![Procesamiento de MAPISendMail en un escenario de WOW64] (media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Procesamiento de MAPISendMail en un escenario de WOW64")
  
## <a name="see-also"></a>Vea también

- [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md)

