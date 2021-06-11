---
title: Probar la implementación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: En este tema se describen algunos escenarios que debe probar con respecto a la instalación y desinstalación de un proveedor Outlook Social Connector (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329165"
---
# <a name="testing-deployment"></a>Probar la implementación

En este tema se describen algunos escenarios que debe probar con respecto a la instalación y desinstalación de un proveedor Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Presencia de Outlook y el OSC en el equipo cliente

Los factores que afectan a la instalación de un proveedor de OSC incluyen la bitness del sistema operativo, la presencia y el bitness de Outlook y el OSC que se habilita en Outlook.
  
Se puede escribir un proveedor de OSC para una versión de 32 o 64 bits del OSC. Outlook 2010 y Outlook 2013 están disponibles en versiones de 32 y 64 bits, y Office Outlook 2003 y Office Outlook 2007 solo están disponibles en versiones de 32 bits. En un sistema operativo Windows de 64 bits, puede instalar un sistema operativo de 32 bits o de 64 Outlook. En un sistema operativo de 32 bits, puede instalar solo 32 bits, pero no 64 bits, Outlook. Según la bitness de la versión instalada de Outlook y el propio proveedor de OSC, el usuario debe usar el instalador adecuado para instalar un proveedor de OSC del bitness adecuado. Por ejemplo, si se instala Outlook de 64 bits y el proveedor de OSC es un componente COM nativo, un proveedor de OSC de 32 bits no funcionará y el usuario debe usar el instalador adecuado para instalar un proveedor de OSC de 64 bits.
  
El código de implementación del proveedor de OSC puede suponer que el usuario tiene una versión compatible de Outlook en el equipo. Sin embargo, si la versión actual de OSC no está en el equipo cliente, el código de implementación puede descargar e instalar una versión adecuada del OSC mediante direcciones URL de vínculo g especialmente construidas en https://g.live.com . Estos vínculos g dependen de la versión y la bits de Outlook y la configuración regional del equipo cliente. Para obtener más información acerca del uso de vínculos g para instalar o actualizar el OSC, vea [Lista de comprobación de instalación](installation-checklist.md).
  
Antes de instalar un proveedor de OSC, el Outlook debe asegurarse de que el complemento OSC está habilitado en Outlook.
  
El método recomendado para implementar un proveedor de OSC es usar un paquete Windows Installer (.msi). Pruebe cada uno de los siguientes escenarios para comprobar que la implementación funciona correctamente para el proveedor.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Outlook no está presente: Outlook 2003 o Outlook 2007 no está instalado y Outlook 2010 o Microsoft Outlook 2013 no está instalado ni ha sido entregado por Hacer clic y ejecutar.  <br/> |Se produce un error en la implementación.  <br/> |
|Outlook 2003 o Outlook 2007 no está instalado, pero Outlook 2010 o Microsoft Outlook 2013 ha sido entregado por Hacer clic y ejecutar.  <br/> |Se implementa el proveedor de 32 bits.  <br/> |
|Outlook 2003 o Outlook 2007 está instalado, pero el OSC no está instalado.  <br/> |El instalador instala el OSC y todas las revisiones. Una vez que el OSC se ha instalado correctamente, el instalador implementa el proveedor.  <br/> |
|Outlook 2003 o Outlook 2007 está instalado y se instala una versión anterior del OSC.  <br/> |El instalador actualiza el OSC, a través de un vínculo g a las revisiones y, a continuación, implementa el proveedor.  <br/> |
|Outlook 2003 o 2007 está instalado y el OSC está actualizado.  <br/> |El instalador implementa el proveedor de 32 bits.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado, pero el OSC no está instalado.  <br/> |Se produce un error en el instalador con un mensaje de error adecuado.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 se instala una versión anterior del OSC.  <br/> |El instalador que es adecuado para la bitness del Outlook instalado 2010 o Microsoft Outlook 2013, actualiza el OSC a través del vínculo g a las revisiones y, a continuación, implementa el proveedor adecuado.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado y el OSC está actualizado.  <br/> |El instalador adecuado para la bitness del Outlook instalado de 2010 o Microsoft Outlook 2013 (32 bits o 64 bits) implementa el proveedor adecuado.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Claves de registro y ubicación instaladas

Compruebe la ubicación del archivo donde se ha implementado el proveedor de OSC y las ubicaciones en el registro Windows donde se crean las claves del Registro para el proveedor.
  
### <a name="file-location-for-osc-provider-dlls"></a>Ubicación de los archivos DLL del proveedor de OSC

Pruebe los escenarios que se enumeran en la tabla siguiente. Tenga en cuenta que la tabla enumera las rutas de instalación predeterminadas para las DLL del proveedor de OSC. Los usuarios pueden personalizar dónde instalan estas DLL.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Microsoft Outlook 2013 está instalado en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en la carpeta Office15. Si el sistema operativo es de 64 bits y Microsoft Outlook 2013 es de 32 bits, las DLL de 32 bits se implementan en C:\Archivos de programa (x86)\Microsoft Office\Office15. Si el sistema operativo es de 64 bits y Microsoft Outlook 2013 es de 64 bits, las DLL de 64 bits se implementan en C:\Archivos de programa\Microsoft Office\Office15. Si el sistema operativo es de 32 bits, las DLL se implementan en C:\Archivos de programa\Microsoft Office\Office15.  <br/> |
|Outlook 2010 está instalado en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en la carpeta Office14. Si el sistema operativo es de 64 bits y Outlook 2010 es de 32 bits, las DLL de 32 bits se implementan en C:\Archivos de programa (x86)\Microsoft Office\Office14. Si el sistema operativo es de 64 bits y Outlook 2010 es de 64 bits, las DLL de 64 bits se implementan en C:\Archivos de programa\Microsoft Office\Office14. Si el sistema operativo es de 32 bits, las DLL se implementan en C:\Archivos de programa\Microsoft Office\Office14.  <br/> |
|Outlook 2007 está instalado en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en C:\Archivos de programa\Microsoft Office\Office14. Al instalar el OSC, se crea la carpeta Office14 y se debe instalar el OSC antes de cualquier DLL del proveedor. Vea la sección anterior [Presencia de Outlook y el OSC en el equipo cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 está instalado en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en C:\Archivos de programa\Microsoft Office\Office14. Al instalar el OSC, se crea la carpeta Office14 y se debe instalar el OSC antes de cualquier DLL del proveedor. Vea la sección anterior [Presencia de Outlook y el OSC en el equipo cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 no está instalado pero entregado por Hacer clic y ejecutar en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en la carpeta Office15. Si el sistema operativo es de 64 bits, las DLL de 32 bits se implementan en C:\Archivos de programa (x86)\Microsoft Office\Office15 o C:\Archivos de programa\Microsoft Office\Office15. Si el sistema operativo es de 32 bits, las DLL se implementan en C:\Archivos de programa\Microsoft Office\Office15. Si la carpeta office15 no existe, la instalación crea la carpeta.  <br/> |
|Outlook 2010 no está instalado, sino entregado por Hacer clic y ejecutar en el equipo cliente.  <br/> |Las DLL de proveedor se implementan en la carpeta Office14. Si el sistema operativo es de 64 bits, las DLL de 32 bits se implementan en C:\Archivos de programa (x86)\Microsoft Office\Office14 o C:\Archivos de programa\Microsoft Office\Office14. Si el sistema operativo es de 32 bits, las DLL se implementan en C:\Archivos de programa\Microsoft Office\Office14. Si la carpeta office14 no existe, la instalación crea la carpeta.  <br/> |
   
### <a name="windows-registry-locations"></a>Windows de registro

Compruebe lo siguiente:
  
- El instalador del proveedor de OSC crea un valor ProgID para el proveedor de OSC en el registro Windows, en cualquiera `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` o `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` . 
    
- La excepción es si el equipo cliente tiene un Outlook de 32 bits en un sistema operativo Windows de 64 bits. En este caso, el ProgID se crea en cualquiera  `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` o  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
- Las claves del Registro deben ser las mismas y en la misma ubicación si, en su lugar, las DLL se registran mediante regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Quitar la instalación

Las siguientes son algunas pruebas para comprobar que el proceso de desinstalación funciona correctamente para el proveedor de OSC.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|El usuario elige desinstalar el proveedor.  <br/> |El proveedor desinstala las DLL y borra el Registro.  <br/> |
|El usuario elige cancelar el proceso de desinstalación del proveedor.  <br/> |El proveedor cancela el proceso de desinstalación y devuelve al usuario al estado antes de que se iniciara el proceso de desinstalación.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Registro de un proveedor](registering-a-provider.md)  
- [Lista de comprobación de instalación](installation-checklist.md)
- [Prepararse para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

