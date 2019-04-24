---
title: Implementación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356920"
---
# <a name="message-service-implementation"></a>Implementación del servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un servicio de mensajes es uno o varios proveedores de servicios relacionados agrupados con el propósito de simplificar la instalación y la configuración. Todos los proveedores de servicios deben incluirse en un servicio de mensajes.
  
Para implementar un servicio de mensajes con uno o más proveedores, use el procedimiento siguiente:
  
1. Diseñar el servicio de mensajes, determinar el número y el tipo de proveedores de servicios que se incluirán. Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [Designing a Message Service](designing-a-message-service.md).
    
2. Cree un programa de instalación para instalar los proveedores de servicios en el servicio de mensajes. Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, consulte [support Message Service Installation](supporting-message-service-installation.md). 
    
3. Cree una función de punto de entrada para realizar la configuración. Para obtener más información acerca de la escritura de una función de punto de entrada del servicio de mensajes, consulte [supportIng Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Cree un archivo de encabezado público que contenga las etiquetas de propiedades y descripciones de los valores válidos para las propiedades personalizadas admitidas por el servicio de mensajes. 
    
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

