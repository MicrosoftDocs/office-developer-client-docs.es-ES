---
title: Desarrollar un proveedor de transporte habilitado para TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f80feecda219e3bcebbf8ceb346b5034e821470
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816669"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desarrollar un proveedor de transporte habilitado para TNEF

  
  
**Hace referencia a**: Outlook 
  
Para promover la interoperabilidad entre los sistemas de mensajería que admiten distintos conjuntos de características MAPI, MAPI proporciona el formato de encapsulación neutro de transporte (TNEF) como una forma estándar para transferir datos. Este formato encapsula las propiedades MAPI no compatibles con un sistema de mensajería subyacente en una secuencia binaria que puede transferirse junto con el mensaje cuando lo envía un proveedor de transporte. El proveedor de transporte que recibe el mensaje, a continuación, puede descodificar la secuencia binaria para recuperar todas las propiedades del mensaje original y que estén disponibles para las aplicaciones cliente. El modelo operativo para TNEF es:
  
- Clientes de mensajería envían y reciban mensajes a un transporte TNEF como normal.
    
- El transporte separa las propiedades de los mensajes salientes en dos categorías: las que admite el sistema de mensaje subyacente y aquellas que no lo hace. Los valores de las propiedades que son compatibles con el sistema de mensajería subyacente se traducen en el formato requerido.
    
- El transporte utiliza los métodos de MAPI TNEF para codificar las propiedades no compatibles en una única secuencia de datos. El transporte, a continuación, convierte esa secuencia de datos en un dato adjunto especial en el mensaje saliente, con el modelo de datos adjuntos del sistema mensajería subyacente, antes de enviar el mensaje.
    
- Un transporte TNEF habilitado que recibe un mensaje de este tipo hace dos cosas. En primer lugar, traduce propiedades del mensaje entrante: los que admite el sistema de mensaje subyacente: en las propiedades MAPI. En segundo lugar, si los datos adjuntos especial está presente, usa los métodos de MAPI TNEF para recuperar propiedades MAPI adicionales de los datos adjuntos antes de entregar el mensaje a una aplicación cliente.
    
MAPI suministra una implementación de la interfaz **ITnef** para su uso por los proveedores de transporte MAPI cuando se trabaja con objetos TNEF. La función [OpenTnefStreamEx](opentnefstreamex.md) se usa para crear objetos TNEF y asociarlos a un mensaje. Las secuencias TNEF se fundamentan en la interfaz **IStream** OLE 
  
> [!NOTE]
> Use **OpenTnefStreamEx** para crear objetos de TNEF. La función **OpenTnefStream** anterior aún existe para la compatibilidad con el código fuente anterior y no debe usarse en cualquier elemento nuevo. 
  
La interfaz de **ITnef** proporciona los siguientes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Es compatible con el modelo de implementación de MAPI TNEF:
  
- Todas las propiedades MAPI sin que ello afecte a otras propiedades del mensaje. En orden para los mensajes MAPI sobrevivir transporte a través de un sistema de mensajería, se deben encapsular todas las propiedades que no se puede codificar como propiedades del sistema de mensajería. Debido a que casi nunca se sabe en el momento en que se envía un mensaje si un cliente compatible con MAPI recibirá el mensaje, la combinación de encapsulación permite a un proveedor de transporte codificar sólo las propiedades de mensaje MAPI que no lo hace el sistema de mensajería admiten de forma nativa. Esto significa que los mensajes que utilice el formato TNEF no son "opacos" para los sistemas de mensajería que no están basados en MAPI, como UNIX basado en SMTP sistemas de mensajería. Estos sistemas recibirán las propiedades que admiten de forma que es habitual para migrarlos y otras propiedades se reciben como una secuencia de datos codificada TNEF. El proveedor de transporte TNEF es responsable de diferenciar entre estos dos conjuntos de propiedades y enviar el conjunto admitido en la manera adecuada para el sistema de mensajería. TNEF no realiza suposiciones sobre el nivel de compatibilidad que proporciona un sistema de mensajería. Sin embargo, en los ejemplos de uso TNEF incluidos en esta sección, se realiza la suposición de, que el sistema de mensajería admite al menos un solo dato adjunto aparte el mensaje. En algunos casos, los datos adjuntos pueden sólo se admite a través de una secuencia en formato UUENCODE y transmite como parte del texto del mensaje. Sólo en circunstancias muy raras el sistema de mensajería tendrá por lo que completa la codificación TNEF de todas las propiedades es necesaria poco soporte para propiedades del mensaje.
    
- Un mecanismo para determinar si una secuencia TNEF en un mensaje entrante pertenece al mensaje, en función de la propiedad MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Esta propiedad debe encontrarse en la secuencia TNEF y en un encabezado de mensaje adecuado. Si la propiedad tiene el mismo valor en ambos lugares, o falta en cualquier lugar, la secuencia TNEF se supone que pertenecen al mensaje. De lo contrario, se omite la secuencia TNEF. Los transportes TNEF habilitado son responsables de la elección de un valor para esta propiedad en los mensajes salientes y codificación en un encabezado de mensaje adecuado (por ejemplo, el identificador de mensaje: encabezado para mensajes SMTP) y en la secuencia TNEF.
    

