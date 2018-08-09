---
title: Probar la implementación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: En este tema se describe algunos escenarios que se deben probar con respecto a la instalación y desinstalación de un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 0494d2ecab446b7da091f80df02267e281987d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821230"
---
# <a name="testing-deployment"></a>Probar la implementación

En este tema se describe algunos escenarios que se deben probar con respecto a la instalación y desinstalación de un proveedor de Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Presencia de Outlook y el OSC en el equipo cliente

Factores de la afectan a la instalación de un proveedor de OSC incluye el valor de bits del sistema operativo, la presencia y valor de bits de Outlook y el OSC está habilitado en Outlook.
  
Para obtener una versión de 32 bits o 64 bits de la OSC se puede escribir un proveedor de OSC. Outlook 2010 y Outlook 2013 están disponibles en versiones de 32 bits y 64 bits, y Office Outlook 2003 y Office Outlook 2007 están disponibles en versiones de 32 bits sólo. En un sistema operativo de Windows de 64 bits, puede instalar Outlook de 32 bits o 64 bits. En un sistema operativo de 32 bits, puede instalar pero no sólo 32 bits, 64 bits, Outlook. Según el valor de bits de la versión instalada de Outlook y el proveedor de OSC propio, el usuario debe usar al instalador adecuado para instalar a un proveedor de OSC del valor de bits adecuada. Por ejemplo, si está instalado Outlook de 64 bits, y el proveedor de OSC es un componente COM nativo, un proveedor OSC de 32 bits no funcionarán y el usuario debe usar al instalador adecuado para instalar a un proveedor OSC de 64 bits.
  
El código de implementación del proveedor de OSC puede asumir que el usuario tiene una versión compatible de Outlook en el equipo. Sin embargo, si la versión actual de OSC no está en el equipo cliente, el código de implementación puede descargar e instalar una versión adecuada de la OSC mediante el uso de las direcciones URL de vínculo de g construidas especialmente en http://g.live.com. Estos vínculos de g dependen de la versión y el valor de bits de Outlook y la configuración regional del equipo cliente. Para obtener más información acerca del uso de vínculos de g para instalar o actualizar el OSC, vea [lista de comprobación de instalación](installation-checklist.md).
  
Antes de instalar a un proveedor de OSC, el usuario de Outlook debe asegurarse de que el complemento de OSC esté habilitado en Outlook.
  
El método recomendado para implementar un proveedor de OSC es usar un paquete de Windows Installer (.msi). Pruebe cada uno de los siguientes escenarios para comprobar funciona la distribución de forma adecuada para el proveedor.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Outlook no está presente: Outlook 2003 u Outlook 2007 no está instalado y Outlook 2010 o Microsoft Outlook 2013 no está instalado ni se ha entregado por Click-to-Run.  <br/> |Se produce un error en la implementación.  <br/> |
|Outlook 2003 u Outlook 2007 no está instalado, pero Outlook 2010 o Microsoft Outlook 2013 se ha entregado por Click-to-Run.  <br/> |Se implementa el proveedor de 32 bits.  <br/> |
|Outlook 2003 u Outlook 2007 está instalado, pero no está instalado el OSC.  <br/> |El instalador se instala el OSC y todas las revisiones. Una vez que el OSC se ha instalado correctamente, el programa de instalación implementa el proveedor.  <br/> |
|Outlook 2003 u Outlook 2007 está instalado y se instala una versión anterior de la OSC.  <br/> |El programa de instalación actualiza el OSC, a través de un vínculo g de revisiones y, a continuación, implementa el proveedor.  <br/> |
|Outlook 2003 o 2007 está instalado y el OSC está actualizado.  <br/> |El instalador de implementa el proveedor de 32 bits.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado pero no está instalado el OSC.  <br/> |Se produce un error en el programa de instalación con un mensaje de error apropiado.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado y se instala una versión anterior de la OSC.  <br/> |El programa de instalación que es el adecuado para el valor de bits de la instalados Outlook 2010 o Microsoft Outlook 2013, actualiza el OSC a través del vínculo de la g a las revisiones y, a continuación, implementa el proveedor adecuado.  <br/> |
|Outlook 2010 o Microsoft Outlook 2013 está instalado y el OSC está actualizado.  <br/> |El programa de instalación que sea apropiado para el valor de bits de la instalados Outlook 2010 o Microsoft Outlook 2013 (32 bits o 64 bits) implementa el proveedor adecuado.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Claves del registro y la ubicación instaladas

Compruebe la ubicación del archivo donde se ha implementado su proveedor de OSC y las ubicaciones en el registro de Windows donde se crean las claves del registro para el proveedor.
  
### <a name="file-location-for-osc-provider-dlls"></a>Ubicación de archivo para archivos DLL de proveedor de OSC

Para los escenarios de prueba que se enumeran en la siguiente tabla. Tenga en cuenta que la tabla se enumeran las rutas de acceso de instalación predeterminada para archivos DLL de proveedor OSC. Los usuarios pueden personalizar donde instalar estos archivos DLL.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Microsoft Outlook 2013 está instalado en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en la carpeta Office15. Si el sistema operativo es de 64 bits y Microsoft Outlook 2013 es de 32 bits, los archivos DLL de 32 bits se implementan en los archivos de C:\Program (x86) \Microsoft Office\Office15. Si el sistema operativo es de 64 bits y 64 bits de es de Microsoft Outlook 2013, los archivos DLL de 64 bits se implementan en C:\Program Files\Microsoft Office\Office15. Si el sistema operativo es de 32 bits, los archivos DLL se implementan en C:\Program Files\Microsoft Office\Office15.  <br/> |
|Outlook 2010 está instalado en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en la carpeta Office14. Si el sistema operativo es de 64 bits y Outlook 2010 es de 32 bits, los archivos DLL de 32 bits se implementan en los archivos de C:\Program (x86) \Microsoft Office\Office14. Si el sistema operativo es de 64 bits y 64 bits de es de Outlook 2010, los archivos DLL de 64 bits se implementan en C:\Program Files\Microsoft Office\Office14. Si el sistema operativo es de 32 bits, los archivos DLL se implementan en C:\Program Files\Microsoft Office\Office14.  <br/> |
|Outlook 2007 está instalado en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en C:\Program Files\Microsoft Office\Office14. Instalar el OSC crea la carpeta de Office14 y el OSC debe instalarse antes de cualquier proveedor de archivos DLL. Vea la sección anterior [presencia de Outlook y el OSC en el equipo a cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 está instalado en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en C:\Program Files\Microsoft Office\Office14. Instalar el OSC crea la carpeta de Office14 y el OSC debe instalarse antes de cualquier proveedor de archivos DLL. Vea la sección anterior [presencia de Outlook y el OSC en el equipo a cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 no está instalado pero entregado por Click-to-Run en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en la carpeta Office15. Si el sistema operativo es de 64 bits, 32 bits archivos DLL se implementan en los archivos de C:\Program (x86) \Microsoft Office\Office15 o C:\Program Files\Microsoft Office\Office15. Si el sistema operativo es de 32 bits, los archivos DLL se implementan en C:\Program Files\Microsoft Office\Office15. Si no existe la carpeta Office15, la instalación crea la carpeta.  <br/> |
|Outlook 2010 no está instalado pero entregado por Click-to-Run en el equipo cliente.  <br/> |Archivos DLL de proveedor se implementan en la carpeta Office14. Si el sistema operativo es de 64 bits, 32 bits archivos DLL se implementan en los archivos de C:\Program (x86) \Microsoft Office\Office14 o C:\Program Files\Microsoft Office\Office14. Si el sistema operativo es de 32 bits, los archivos DLL se implementan en C:\Program Files\Microsoft Office\Office14. Si no existe la carpeta de Office14, la instalación crea la carpeta.  <br/> |
   
### <a name="windows-registry-locations"></a>Ubicaciones del registro de Windows

Compruebe lo siguiente:
  
- El programa de instalación del proveedor OSC crea un valor ProgID para el proveedor de OSC en el registro de Windows en cualquiera `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` o `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`. 
    
- La excepción es si el equipo cliente tiene Outlook de 32 bits que se ejecutan en un sistema operativo de Windows de 64 bits. En este caso, se crea el ProgID en cualquiera `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` o `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Las claves del registro deben ser el mismo y en la misma ubicación si, en su lugar, se registran las DLL mediante regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Eliminación de la instalación

Las siguientes son algunas pruebas para comprobar que el proceso de desinstalación funciona correctamente para su proveedor de OSC.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|El usuario elige desinstalar el proveedor.  <br/> |El proveedor desinstala los archivos DLL y borra el registro.  <br/> |
|El usuario elige cancelar el proceso de desinstalación del proveedor.  <br/> |El proveedor cancela el proceso de desinstalación y le lleva al usuario al estado antes de iniciar el proceso de desinstalación.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Registrar un proveedor](registering-a-provider.md)  
- [Lista de comprobación de instalación](installation-checklist.md)
- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

