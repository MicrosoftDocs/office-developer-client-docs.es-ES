---
title: Implementación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818389"
---
# <a name="message-service-implementation"></a>Implementación del servicio de mensajes

  
  
**Se aplica a**: Outlook 
  
Un servicio de mensajes es uno o más proveedores de servicios relacionadas agrupados con el propósito de simplificar la instalación y configuración. Todos los proveedores de servicios deben incluirse en un servicio de mensajes.
  
Para implementar un servicio de mensajes con uno o varios proveedores, use el procedimiento siguiente:
  
1. Diseñar el servicio de mensajes, determinar el número y el tipo de proveedores de servicios que se incluya. Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [diseñar un servicio de mensajes](designing-a-message-service.md).
    
2. Crear un programa de instalación para instalar a los proveedores de servicios en el servicio de mensajes. Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, vea [Compatibilidad con mensaje de servicio de instalación](supporting-message-service-installation.md). 
    
3. Crear una función de punto de entrada para realizar la configuración. Para obtener más información acerca de cómo escribir una entrada de mensajes de servicio de función de punto, vea [Compatibilidad con configuración del servicio de mensajes](supporting-message-service-configuration.md) y [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Cree un archivo de encabezado público que contiene las etiquetas de propiedad y descripciones de los valores válidos para las propiedades personalizadas que es compatible con el servicio de mensajes. 
    
## <a name="see-also"></a>Ver también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

