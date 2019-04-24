---
title: Probar la implementación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: En este tema se describen algunos escenarios que debe probar con respecto a la instalación y desinstalación de un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329165"
---
# <a name="testing-deployment"></a>Probar la implementación

En este tema se describen algunos escenarios que debe probar con respecto a la instalación y desinstalación de un proveedor de Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Presencia de Outlook y OSC en el equipo cliente

Factores el efecto que tiene la instalación de un proveedor OSC incluye los bits del sistema operativo, la presencia y el bits de Outlook, y el OSC habilitado en Outlook.
  
Se puede escribir un proveedor OSC para una versión de 32 bits o de 64 bits del OSC. Outlook 2010 y Outlook 2013 están disponibles en las versiones de 32 y 64 bits, y Office Outlook 2003 y Office Outlook 2007 solo están disponibles en versiones de 32 bits. En un sistema operativo Windows de 64 bits, puede instalar las opciones de Outlook de 32 bits o de 64 bits. En un sistema operativo de 32 bits, puede instalar solo 32 bits, pero sin 64 bits, Outlook. Según el bits de la versión instalada de Outlook y el propio proveedor OSC, el usuario debe usar el instalador adecuado para instalar un proveedor de OSC del bits correspondiente. Por ejemplo, si está instalado Outlook de 64 bits, y el proveedor de OSC es un componente COM nativo, un proveedor de OSC de 32 bits no funcionará y el usuario debe usar el instalador adecuado para instalar un proveedor OSC de 64 bits.
  
El código de implementación del proveedor de OSC puede suponer que el usuario tiene una versión de Outlook en el equipo compatible. Sin embargo, si la versión actual de OSC no está en el equipo cliente, el código de implementación puede descargar e instalar una versión adecuada del OSC mediante direcciones URL de g-Link construidas especialmente en https://g.live.com. Estos g-links dependen de la versión y el bits de Outlook y la configuración regional del equipo cliente. Para obtener más información acerca de cómo usar g-links para instalar o actualizar el OSC, consulte [Installation Checklist](installation-checklist.md).
  
Antes de instalar un proveedor OSC, el usuario de Outlook debe asegurarse de que el complemento OSC esté habilitado en Outlook.
  
El método recomendado para implementar un proveedor de OSC es usar un paquete de Windows Installer (. msi). Pruebe cada uno de los siguientes escenarios para comprobar que la implementación funciona correctamente para el proveedor.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Outlook no está presente: Outlook 2003 o Outlook 2007 no está instalado, y Outlook 2010 o Microsoft Outlook 2013 no se ha instalado, ni se ha entregado mediante hacer clic y ejecutar.  <br/> |Se produce un error en la implementación.  <br/> |
|Outlook 2003 o Outlook 2007 no está instalado, pero Outlook 2010 o Microsoft Outlook 2013 han sido entregados por hacer clic y ejecutar.  <br/> |Se implementa el proveedor de 32 bits.  <br/> |
|Outlook 2003 o Outlook 2007 está instalado, pero el OSC no está instalado.  <br/> |El instalador instala el OSC y todas las revisiones. Una vez que se ha instalado correctamente el OSC, el instalador implementa el proveedor.  <br/> |
|Outlook 2003 o Outlook 2007 está instalado y hay instalada una versión anterior del OSC.  <br/> |El instalador actualiza el OSC, a través de un g-Link a patches y, a continuación, implementa el proveedor.  <br/> |
|Outlook 2003 o 2007 está instalado y el OSC está actualizado.  <br/> |El instalador implementa el proveedor de 32 bits.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado pero el OSC no está instalado.  <br/> |El instalador da error con un mensaje de error adecuado.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado y se ha instalado una versión anterior del OSC.  <br/> |El instalador que es apropiado para el bits de la instalación de Outlook 2010 o Microsoft Outlook 2013, actualiza el OSC mediante el vínculo g a patches y, a continuación, implementa el proveedor correspondiente.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado y el OSC está actualizado.  <br/> |El instalador apropiado para el bits de la Outlook 2010 o Microsoft Outlook 2013 (32-bit o 64-bit) instalado implementa el proveedor correspondiente.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Ubicación de instalación y claves del registro

Compruebe la ubicación del archivo en el que se ha implementado el proveedor de OSC y las ubicaciones en el registro de Windows en las que se crean las claves del registro para el proveedor.
  
### <a name="file-location-for-osc-provider-dlls"></a>Ubicación del archivo para los archivos DLL del proveedor OSC

Pruebe los escenarios que se muestran en la tabla siguiente. Tenga en cuenta que en la tabla se enumeran las rutas de instalación predeterminadas para los archivos DLL del proveedor OSC. Los usuarios pueden personalizar dónde instalan estos archivos dll.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Microsoft Outlook 2013 está instalado en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en la carpeta Office15 Si el sistema operativo es 64 bits y Microsoft Outlook 2013 es 32 bits, las dll de 32 bits se implementan en C:\Archivos de programa (x86) \Microsoft Office\Office15. Si el sistema operativo es 64 bits y Microsoft Outlook 2013 es 64 bits, las dll de 64 bits se implementan en C:\Archivos de Programa\microsoft Office\Office15. Si el sistema operativo es 32 bits, los archivos DLL se implementan en C:\Archivos de Programa\microsoft Office\Office15.  <br/> |
|Outlook 2010 está instalado en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en la carpeta Office14. Si el sistema operativo es 64 bits y Outlook 2010 es 32 bits, las dll de 32 bits se implementan en C:\Archivos de programa (x86) \Microsoft Office\Office14. Si el sistema operativo es 64 bits y Outlook 2010 es 64 bits, las dll de 64 bits se implementan en C:\Archivos de Programa\microsoft Office\Office14. Si el sistema operativo es 32 bits, los archivos DLL se implementan en C:\Archivos de Programa\microsoft Office\Office14.  <br/> |
|Outlook 2007 está instalado en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en C:\Archivos de Programa\microsoft Office\Office14. La instalación del OSC crea la carpeta Office14 y el OSC debe instalarse antes que cualquier dll de proveedor. Vea la sección anterior [de la presencia de Outlook y el OSC en el equipo cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 está instalado en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en C:\Archivos de Programa\microsoft Office\Office14. La instalación del OSC crea la carpeta Office14 y el OSC debe instalarse antes que cualquier dll de proveedor. Vea la sección anterior [de la presencia de Outlook y el OSC en el equipo cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 no está instalado, pero lo proporciona hacer clic y ejecutar en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en la carpeta Office15 Si el sistema operativo es 64, se implementan dll de 32 bits en C:\Program Files (x86) \Microsoft Office\Office15 o en C:\Archivos de Programa\microsoft Office\Office15. Si el sistema operativo es 32 bits, los archivos DLL se implementan en C:\Archivos de Programa\microsoft Office\Office15. Si la carpeta Office15 no existe, la instalación crea la carpeta.  <br/> |
|Outlook 2010 no está instalado, pero lo proporciona hacer clic y ejecutar en el equipo cliente.  <br/> |Las DLL del proveedor se implementan en la carpeta Office14. Si el sistema operativo es 64, se implementan dll de 32 bits en C:\Program Files (x86) \Microsoft Office\Office14 o en C:\Archivos de Programa\microsoft Office\Office14. Si el sistema operativo es 32 bits, los archivos DLL se implementan en C:\Archivos de Programa\microsoft Office\Office14. Si la carpeta Office14 no existe, la instalación crea la carpeta.  <br/> |
   
### <a name="windows-registry-locations"></a>Ubicaciones del registro de Windows

Compruebe lo siguiente:
  
- El instalador del proveedor OSC crea un valor ProgID para el proveedor OSC en el registro de Windows, `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` en `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`o. 
    
- La excepción es cuando el equipo cliente tiene Outlook de 32 bits ejecutándose en un sistema operativo Windows de 64 bits. En este caso, el ProgID se crea en `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` o. `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- Las claves del registro deben ser las mismas y estar en la misma ubicación si, en su lugar, los archivos dll los registra regsvr32. exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Eliminación de la instalación

Las siguientes son algunas pruebas para comprobar que el proceso de desinstalación funciona correctamente para su proveedor de OSC.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|El usuario elige desinstalar el proveedor.  <br/> |El proveedor desinstala los archivos dll y borra el registro.  <br/> |
|El usuario decide cancelar el proceso de desinstalación del proveedor.  <br/> |El proveedor cancela el proceso de desinstalación y devuelve el usuario al estado anterior al inicio del proceso de desinstalación.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Registrar un proveedor](registering-a-provider.md)  
- [Lista de comprobación de instalación](installation-checklist.md)
- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

