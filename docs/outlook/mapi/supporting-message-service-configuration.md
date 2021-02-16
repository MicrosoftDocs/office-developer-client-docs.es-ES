---
title: Admitir la configuración del servicio de soporte mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418998"
---
# <a name="supporting-message-service-configuration"></a>Admitir la configuración del servicio de soporte mensaje
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para admitir la configuración del servicio de mensajes, use el siguiente procedimiento:
  
1. Implementar una función de punto de entrada que se ajuste al prototipo [MSGSERVICEENTRY.](msgserviceentry.md) Las funciones de punto de entrada del servicio de mensajes administran el acceso a los datos de configuración y se les llama en las siguientes circunstancias: 
    
   - Cuando un cliente inicia sesión para recuperar información para configurar el servicio de mensajes.
    
   - Cuando un cliente desea ver o cambiar una propiedad de configuración. 
    
   Aunque la mayoría de los servicios de mensajes proporcionarán funciones de punto de entrada, como deberían, estas funciones no son estrictamente necesarias. Los servicios de mensajes pueden proporcionar acceso a los datos de configuración de otras maneras. Sin embargo, el uso de una función de punto de entrada estandariza y simplifica el proceso de configuración.
    
   MAPI espera que todas las funciones de punto de entrada del servicio de mensajes puedan almacenar y recuperar propiedades de las secciones de perfil asociadas a su servicio de mensajes. Puede admitir esta funcionalidad de forma interactiva, mediante programación o tanto de forma interactiva como mediante programación.
    
   Para admitir la configuración interactiva, proporcione una hoja de propiedades que muestre las propiedades implicadas en la configuración del servicio de mensajes. Como opción, también puede proporcionar hojas de propiedades para cada proveedor configurable. Algunos servicios de mensajes restringen a los usuarios a una vista de solo lectura de las propiedades de configuración; otros servicios de mensajes permiten a los usuarios realizar cambios.
    
   Para admitir la configuración mediante programación, la función de punto de entrada del servicio de mensajes debe poder funcionar sin la intervención del usuario. Si el Asistente para perfiles puede llamar al servicio de mensajes, debe admitir la configuración mediante programación. Si el servicio de mensajes no se permite configurar mediante el Asistente para perfiles, puede elegir si desea admitir o no la configuración mediante programación.
    
   Para obtener más información acerca de cómo admitir la configuración en una función de punto de entrada del servicio de mensajes, vea [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publique el nombre de la función de punto de entrada del servicio de mensajes en el archivo de configuración Mapisvc.inf incluyendo la siguiente entrada en la sección de servicio de mensajes:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Cree uno o más cuadros de diálogo de hoja de propiedades para mostrar los datos de configuración.
    
4. Realice las siguientes tareas si desea permitir que el Asistente para perfiles configure el servicio de mensajes:
    
   - Implementar una función de punto de entrada que se ajuste al prototipo [WIZARDENTRY.](wizardentry.md) 
    
   - Implemente un procedimiento de cuadro de diálogo estándar de Windows que se ajuste al prototipo [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md) 
    
   - Mejore la función de punto de entrada del servicio de mensajes para responder a eventos adicionales.
    
## <a name="see-also"></a>Consulte también

- [Implementación del servicio de mensajes](message-service-implementation.md)

