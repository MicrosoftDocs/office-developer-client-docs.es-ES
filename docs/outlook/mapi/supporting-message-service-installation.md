---
title: Compatibilidad con la instalación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820799"
---
# <a name="supporting-message-service-installation"></a>Compatibilidad con la instalación del servicio de mensajes

  
  
**Se aplica a**: Outlook 
  
El programa de instalación para instalar el servicio de mensajes debe hacer lo siguiente:
  
1. Copie los archivos de servicio de mensajes, como el servicio de mensajes y el proveedor de servicios de archivos DLL, desde un CD o disco, en una unidad local en la estación de trabajo. Los archivos que deben copiarse dependen de su servicio de mensajes. Normalmente se copie al menos una DLL.
    
2. Agregar entradas al archivo de configuración Mapisvc.inf. Para obtener más información acerca de cómo modificar este archivo para admitir los proveedores de servicios en el servicio de mensajes, vea [Formato de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Agregar entradas, según corresponda, en el registro del sistema para servicios de mensajes. Para obtener más información acerca de cómo deben aparecer las entradas en el registro del sistema, vea [instalar el subsistema MAPI](installing-the-mapi-subsystem.md).
    
4. Crear un perfil predeterminado si no existe todavía mediante uno de los siguientes elementos:
    
  - El Asistente para perfiles para crear un perfil mediante el uso de interacción del usuario a través de una serie de cuadros de diálogo. Para obtener más información acerca de cómo utilizar al Asistente para perfiles, vea [creación de un perfil mediante el Asistente para perfiles](creating-a-profile-by-using-the-profile-wizard.md).
    
  - El Panel de Control para crear un perfil mediante el uso de interacción del usuario. El Panel de Control ofrece al usuario más flexibilidad que el Asistente para perfiles para configurar los servicios de mensaje y establecer las propiedades de perfil. 
    
Colocar el programa de instalación en un directorio público designado. Esto es importante porque la mayoría de los clientes de configuración, como el Panel de Control, requieren que los usuarios escribir el nombre del directorio. El Panel de Control invoca un programa de instalación cuando un usuario hace clic en el botón **Agregar** , invoca el cuadro de diálogo **Utilizar disco** y especifica la ruta de acceso al programa. El Panel de Control se ejecuta el programa y llama a la función de punto de entrada del servicio de su mensaje con el parámetro _ulContext_ establecido en MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Dado que los perfiles son un elemento prescindibles de la arquitectura MAPI, asegúrese de que el programa de instalación no almacenar nada en el perfil predeterminado que sería difícil de volver a crear. No hay ningún utilidades para la recuperación de perfil, para mover los perfiles de un equipo a otro, de copia de seguridad sin conexión o para la restauración individual o global de copias de seguridad. 
  
## <a name="see-also"></a>Ver también



[Implementación del servicio de mensajes](message-service-implementation.md)

