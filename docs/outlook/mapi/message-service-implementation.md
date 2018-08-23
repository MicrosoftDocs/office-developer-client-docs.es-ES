---
title: Implementación de servicios de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c7007c01803676412b3efca8b7825b2ed8d863e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582486"
---
# <a name="message-service-implementation"></a>Implementación de servicios de mensajería

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un servicio de mensajes es uno o más proveedores de servicios relacionadas agrupados con el propósito de simplificar la instalación y configuración. Todos los proveedores de servicios deben incluirse en un servicio de mensajes.
  
Para implementar un servicio de mensajes con uno o varios proveedores, use el procedimiento siguiente:
  
1. Diseñar el servicio de mensajes, determinar el número y el tipo de proveedores de servicios que se incluya. Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [diseñar un servicio de mensajes](designing-a-message-service.md).
    
2. Crear un programa de instalación para instalar a los proveedores de servicios en el servicio de mensajes. Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, vea [Compatibilidad con mensaje de servicio de instalación](supporting-message-service-installation.md). 
    
3. Crear una función de punto de entrada para realizar la configuración. Para obtener más información acerca de cómo escribir una entrada de mensajes de servicio de función de punto, vea [Compatibilidad con configuración del servicio de mensajes](supporting-message-service-configuration.md) y [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Cree un archivo de encabezado público que contiene las etiquetas de propiedad y descripciones de los valores válidos para las propiedades personalizadas que es compatible con el servicio de mensajes. 
    
## <a name="see-also"></a>Recursos adicionales



[Proveedores de servicios de MAPI](mapi-service-providers.md)

