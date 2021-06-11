---
title: Compatibilidad con la instalación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404704"
---
# <a name="supporting-message-service-installation"></a>Compatibilidad con la instalación del servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El programa de instalación para instalar el servicio de mensajes debe hacer lo siguiente:
  
1. Copie los archivos de servicio de mensajes, como los ARCHIVOS DLL del servicio de mensajes y del proveedor de servicios, desde un CD o disco, a una unidad local de la estación de trabajo. Los archivos que deben copiarse dependen del servicio de mensajes. Normalmente, copiará al menos una DLL.
    
2. Agregue entradas al archivo de configuración Mapisvc.inf. Para obtener más información acerca de cómo modificar este archivo para admitir los proveedores de servicios en el servicio de mensajes, vea Formato de archivo [de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Agregue entradas, según corresponda, al Registro del sistema para los servicios de mensajes. Para obtener más información acerca de cómo deben aparecer las entradas en el Registro del sistema, vea [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).
    
4. Cree un perfil predeterminado si aún no existe mediante uno de los siguientes elementos:
    
  - Asistente para perfiles para crear un perfil mediante la interacción del usuario a través de una serie de cuadros de diálogo. Para obtener más información acerca del uso del Asistente para perfiles, vea [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Panel de control para crear un perfil mediante la interacción del usuario. El Panel de control ofrece al usuario más flexibilidad que el Asistente para perfiles para configurar los servicios de mensajes y establecer las propiedades del perfil. 
    
Coloque el programa de instalación en un directorio público designado. Esto es importante porque la mayoría de los clientes de configuración, como el Panel de control, requieren que los usuarios escriban el nombre del directorio. El Panel de control invoca un programa  de instalación cuando un usuario hace clic en el botón Agregar, invoca el cuadro de diálogo **Tener** disco y especifica la ruta de acceso al programa. El Panel de control ejecuta el programa y llama a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Dado que los perfiles son una parte prescindible de la arquitectura MAPI, asegúrese de que el programa de instalación no almacena nada en el perfil predeterminado que sería difícil volver a crear. No hay utilidades para la recuperación de perfiles, para mover perfiles de un equipo a otro, para la copia de seguridad fuera de línea o para la restauración individual o global de copias de seguridad. 
  
## <a name="see-also"></a>Vea también



[Implementación del servicio de mensajes](message-service-implementation.md)

