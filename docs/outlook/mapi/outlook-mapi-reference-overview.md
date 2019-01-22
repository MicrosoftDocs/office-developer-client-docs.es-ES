---
title: Información general de la referencia MAPI de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificación: 1 de febrero de 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723022"
---
# <a name="outlook-mapi-reference-overview"></a>Información general de la referencia MAPI de Outlook

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Este artículo proporciona información general sobre la documentación de la referencia MAPI de Outlook 2013.
  
## <a name="about-this-documentation"></a>Acerca de esta documentación

Esta documentación hace referencia a la implementación de la API de mensajería (MAPI) de Microsoft Outlook 2013. 
  
Antes de Microsoft Office Outlook 2007, la referencia del programador de MAPI formaba parte de la documentación de Microsoft Exchange.
  
> [!NOTE]
> Dado que Exchange ha restado protagonismo al uso de MAPI desde el lanzamiento de Microsoft Exchange Server 2007, la compatibilidad con la implementación de Exchange es bastante limitada. 
  
La implementación de Outlook de MAPI difiere de la implementación de Microsoft Exchange. La implementación de Outlook está optimizada para ejecutarse en los equipos cliente y destaca la baja latencia. La implementación de Exchange está destinada a los servidores donde la alta disponibilidad y un mejor multiproceso son importantes.
  
Use esta documentación para aplicaciones que se ejecuten en los sistemas del usuario final. Para las aplicaciones de servidor, utilice la implementación de Exchange de MAPI, si corresponde, o las API actuales de Exchange como, por ejemplo, los Servicios Web de Exchange. Para más información sobre los Servicios Web de Exchange, consulte la [Referencia de Servicios Web de Exchange](https://msdn.microsoft.com/library/bb204119.aspx).
  
Es posible escribir aplicaciones que funcionen tanto con las implementaciones de MAPI de Outlook como con las de Exchange. Por ejemplo, MFCMAPI funciona correctamente en ambas plataformas. Las implementaciones tienen muchas características comunes, pero también hay diferencias, algunas sutiles y otras más evidentes. Tendrá que probar cuidadosamente en ambas plataformas si tiene la intención de trabajar con la aplicación en todos los entornos. Esta prueba requiere dos sistemas, puesto que no se admite la ejecución de ambas implementaciones en la misma instalación de sistema operativo.
  
Tenga en cuenta que MAPI es adecuado para el acceso de bajo nivel a datos en un almacén de MAPI o para crear un proveedor de transporte, de almacén de mensajes o de libreta de direcciones. Puesto que MAPI omite la lógica de negocios de Outlook, debería considerar también el uso del modelo de objetos de Outlook al evaluar las API para crear una solución. El modelo de objetos de Outlook encapsula la lógica de negocios de Outlook, pero no es adecuado para el código multiproceso, los proveedores de sincronización ni las aplicaciones de servicio de Windows.
  
Para obtener más información sobre las novedades de esta edición, consulte los siguientes temas:
  
- [Novedades de esta edición](what-s-new-in-this-edition.md)
    
- [Elementos de la API que se dejan de usar en esta edición](api-elements-deprecated-in-this-edition.md)
    
Si tiene poca experiencia en el desarrollo de aplicaciones MAPI para Outlook, consulte los temas siguientes:
  
- [Seleccionar una API o tecnología para desarrollar soluciones de Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [Archivos de encabezado de uso frecuente](commonly-used-header-files.md)
    
- [Propiedades de uso frecuente](commonly-used-properties.md)
    
- [Objetos de uso frecuente](commonly-used-objects.md)
    
El resto de esta referencia se clasifica en los siguientes tres tipos de información:
  
- [Ejemplos de MAPI](mapi-samples.md): le dirige a muchos ejemplos de código que muestran el uso de varios elementos de la API y cómo implementar proveedores básicos de MAPI y crear elementos de Outlook. 
    
- [Conceptos de MAPI](mapi-concepts.md): explica los conceptos y la arquitectura de MAPI. 
    
- [Referencia MAPI](mapi-reference.md): proporciona información detallada sobre las funciones, interfaces, estructuras y propiedades de MAPI. 
    
## <a name="see-also"></a>Vea también

- [Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
- [Ejemplos de MAPI](mapi-samples.md)
- [Conceptos de MAPI](mapi-concepts.md)

