---
title: Información general de la referencia MAPI de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificación: 01 de febrero de 2013'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818454"
---
# <a name="outlook-mapi-reference-overview"></a>Información general de la referencia MAPI de Outlook

**Hace referencia a**: Outlook 
  
En este tema se proporciona información general sobre la documentación de referencia de MAPI de Outlook 2013.
  
## <a name="about-this-documentation"></a>Acerca de esta documentación

Esta documentación se aplica a la implementación de la mensajería API (MAPI) de Microsoft Outlook 2013. 
  
Anteriores a Microsoft Office Outlook 2007, referencia del programador de MAPI formaba parte de la documentación de Microsoft Exchange.
  
> [!NOTE]
> Debido a que Exchange ha deemphasized el uso de MAPI desde Microsoft Exchange Server 2007, la compatibilidad con la implementación de Exchange está limitada. 
  
La implementación de Outlook de MAPI difiere de la implementación de Microsoft Exchange. La implementación de Outlook está optimizada para que se ejecutan en los equipos cliente y enfatiza baja latencia. La implementación de Exchange está pensada para los servidores donde una alta disponibilidad y mejor multithreading son importantes.
  
Utilice esta documentación para aplicaciones que se ejecutan en sistemas de usuario final. Para aplicaciones de servidor, use la implementación de Exchange de MAPI si es necesario o usar las API de Exchange actual, como los servicios Web Exchange. Para obtener más información sobre los servicios Web Exchange, vea la [Referencia de servicios Web de Exchange](http://msdn.microsoft.com/en-us/library/bb204119.aspx).
  
Es posible escribir aplicaciones que funcionan con las implementaciones de Outlook ni en Exchange de MAPI. Por ejemplo, MFCMAPI funciona bien en cualquier plataforma. Las implementaciones tienen muchas características comunes, pero existen diferencias sutiles y evidente. Debe probar detenidamente en ambas plataformas, si tiene intención de su aplicación para que funcionen en todos los entornos. Esta prueba requiere dos sistemas porque no se admite la ejecución de ambas implementaciones en la misma instalación de sistema operativo.
  
Tenga en cuenta que es apropiada para el acceso a datos en un almacén MAPI de bajo nivel o la creación de un transporte, el almacén de mensajes o el proveedor de la libreta de direcciones MAPI. Dado que MAPI omite la lógica de negocios de Outlook, también debe considerar el uso del modelo de objetos de Outlook al evaluar las API para la creación de la solución. El modelo de objetos de Outlook encapsular la lógica de negocios de Outlook pero no es adecuado para aplicaciones de servicio de Windows, los proveedores de sincronización o código multiproceso.
  
Para obtener información acerca de cuáles son las novedades de esta edición, vea los temas siguientes:
  
- [Novedades de esta edición](what-s-new-in-this-edition.md)
    
- [Elementos de la API que se dejan de usar en esta edición](api-elements-deprecated-in-this-edition.md)
    
Si está familiarizado con desarrollo de aplicaciones de MAPI para Outlook, vea los temas siguientes:
  
- [Seleccionar una API o tecnología para desarrollar soluciones para Outlook 2013](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [Archivos de encabezado de uso frecuente](commonly-used-header-files.md)
    
- [Propiedades de uso frecuente](commonly-used-properties.md)
    
- [Objetos de uso frecuente](commonly-used-objects.md)
    
El resto de esta referencia se clasifica en los siguientes tres tipos de información:
  
- [Ejemplos de MAPI](mapi-samples.md) - le dirige a muchos de los ejemplos de código que muestran el uso de diversos elementos de la API y cómo implementar proveedores MAPI básicos y crear elementos de Outlook. 
    
- [Conceptos de MAPI](mapi-concepts.md) - explica los conceptos y la arquitectura de MAPI. 
    
- [Referencia de la MAPI](mapi-reference.md) - proporciona información detallada sobre las funciones, interfaces, estructuras y las propiedades de MAPI. 
    
## <a name="see-also"></a>Vea también

- [Introducción a la referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
- [Ejemplos de MAPI](mapi-samples.md)
- [Conceptos MAPI](mapi-concepts.md)

