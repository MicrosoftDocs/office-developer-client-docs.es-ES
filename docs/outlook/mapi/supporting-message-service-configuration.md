---
title: Compatibilidad con la configuración del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6f9ac5d9cef09ce6d4f3006ecc804db6291cae77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579343"
---
# <a name="supporting-message-service-configuration"></a>Compatibilidad con la configuración del servicio de mensajes
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para admitir la configuración del servicio de mensajes, use el procedimiento siguiente:
  
1. Implementar una función de punto de entrada que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) . Funciones de punto de entrada de servicio de mensaje administración el acceso a datos de configuración y se denominan en las siguientes circunstancias: 
    
   - Cuando un cliente inicia sesión para recuperar información para configurar el servicio de mensajes.
    
   - Cuando un cliente desea ver o cambiar una propiedad de configuración. 
    
   Aunque la mayoría de los servicios de mensaje proporcionará las funciones de punto de entrada, como deberían, estas funciones no son estrictamente necesarias. Servicios de mensajes pueden proporcionar acceso a datos de configuración de otras maneras. Sin embargo, el uso de una función de punto de entrada estandariza y simplifica el proceso de configuración.
    
   MAPI espera que funciones del punto de entrada de servicio de todos los mensajes que puedan almacenar y recuperar las propiedades de las secciones de perfil que están asociadas con su servicio de mensajes. Puede admitir esta funcionalidad de forma interactiva, mediante programación, o ambos de forma interactiva y mediante programación.
    
   Para admitir la configuración interactiva, proporcionar una hoja de propiedades que se muestran las propiedades necesarios para configurar el servicio de mensajes. Como una opción, también puede proporcionar las hojas de propiedades para cada proveedor configurable. Algunos servicios de mensaje restricción a los usuarios a una vista de solo lectura de propiedades de configuración; otros servicios de mensaje permiten a los usuarios realizar cambios.
    
   Para admitir la configuración mediante programación, la función de punto de entrada de servicio de mensaje debe poder funcionar sin intervención del usuario. Si el servicio de mensajes se puede llamar mediante el Asistente para perfiles, debe admitir la configuración mediante programación. Si el servicio de mensajes no permitir que se pueden configurar mediante el Asistente para perfiles, puede elegir si desea o no admite la configuración mediante programación.
    
   Para obtener más información acerca de cómo admitir la configuración en una entrada de mensajes de servicio punto (función), consulte [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publicar el nombre de la función de punto de entrada de servicio de mensaje en el archivo de configuración Mapisvc.inf mediante la inclusión de la siguiente entrada en la sección servicio de mensaje:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Crear uno o varios (propiedad) hoja cuadros de diálogo para mostrar los datos de configuración.
    
4. Si desea permitir que el Asistente para perfiles configurar el servicio de mensajes, realice las siguientes tareas:
    
   - Implementar una función de punto de entrada que se ajusta al prototipo [WIZARDENTRY](wizardentry.md) . 
    
   - Implementar un procedimiento de cuadros de diálogo de Windows estándar que se ajusta al prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
    
   - Mejorar la función de punto de entrada de servicio de mensaje para responder a eventos adicionales.
    
## <a name="see-also"></a>Recursos adicionales

- [Implementación de servicios de mensajería](message-service-implementation.md)

