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
ms.openlocfilehash: 282b1866699b695c647caedd130ce5abc1bcbc2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316698"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desarrollar un proveedor de transporte habilitado para TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para promover la interoperabilidad entre sistemas de mensajería que admiten distintos conjuntos de características de MAPI, MAPI proporciona el formato de encapsulación neutro para el transporte (TNEF) como una forma estándar de transferir datos. Este formato encapsula las propiedades MAPI no admitidas por un sistema de mensajería subyacente en una secuencia binaria que se puede transferir junto con el mensaje cuando lo envía un proveedor de transporte. A continuación, el proveedor de transporte que recibe el mensaje puede descodificar la secuencia binaria para recuperar todas las propiedades del mensaje original y hacer que estén disponibles para las aplicaciones cliente. El modelo operativo de TNEF es:
  
- Los clientes de mensajería envían y reciben mensajes en un transporte TNEF de la forma habitual.
    
- El transporte separa las propiedades de los mensajes salientes en dos categorías: las que admite el sistema de mensajes subyacente y las que no lo son. Los valores de las propiedades que son compatibles con el sistema de mensajería subyacente se traducen al formato requerido.
    
- El transporte usa los métodos de MAPI TNEF para codificar las propiedades no admitidas en una única secuencia de datos. A continuación, el transporte convierte esa secuencia de datos en un dato adjunto especial en el mensaje saliente, usando el modelo de datos adjuntos del sistema de mensajería subyacente, antes de enviar el mensaje.
    
- Un transporte habilitado para TNEF que recibe un mensaje de este tipo hace dos cosas. En primer lugar, traduce las propiedades del mensaje entrante, las que son compatibles con el sistema de mensajes subyacente, en las propiedades MAPI. En segundo lugar, si los datos adjuntos especiales están presentes, usa los métodos MAPI TNEF para recuperar propiedades MAPI adicionales de los datos adjuntos antes de entregar el mensaje a una aplicación cliente.
    
MAPI proporciona una implementación de la interfaz **ITnef** para que la usen los proveedores de transporte MAPI cuando trabaja con objetos TNEF. La función [OpenTnefStreamEx](opentnefstreamex.md) se usa para crear objetos TNEF y asociarlos a un mensaje. Las secuencias TNEF se crean sobre la interfaz OLE **IStream** 
  
> [!NOTE]
> Use **OpenTnefStreamEx** para crear objetos TNEF. La función **OpenTnefStream** antigua todavía existe para la compatibilidad con el código fuente antiguo y no debe usarse en nada nuevo. 
  
La interfaz **ITnef** proporciona los siguientes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
El modelo de implementación de MAPI TNEF admite:
  
- Todas las propiedades MAPI sin afectar a otras propiedades del mensaje. Para que los mensajes MAPI puedan sobrevivir al transporte a través de un sistema de mensajería, se deben encapsular todas las propiedades que no se pueden codificar como propiedades del sistema de mensajería. Debido a que casi nunca se conoce en el momento en el que se envía un mensaje si un cliente compatible con MAPI recibirá el mensaje, el esquema de encapsulación permite que un proveedor de transporte codifique solo las propiedades de mensaje MAPI que el sistema de mensajería no compatibilidad de forma nativa. Esto significa que los mensajes que utilizan TNEF no son "opacos" a los sistemas de mensajería que no se basan en MAPI, como los sistemas de mensajería UNIX basados en SMTP. Estos sistemas reciben las propiedades que admiten de la manera típica para ellos, y otras propiedades se reciben como una secuencia de datos TNEF codificada. El proveedor de transporte TNEF es responsable de diferenciar estos dos conjuntos de propiedades y enviar el conjunto admitido de la manera adecuada para el sistema de mensajería. TNEF no asume nada en cuanto al nivel de compatibilidad que proporciona un sistema de mensajería. Sin embargo, en los ejemplos de uso de TNEF incluidos en esta sección, se supone que el sistema de mensajería admite al menos un solo dato adjunto del mensaje. En algunos casos, los datos adjuntos solo pueden admitirse a través de una secuencia UUEncoded y transmitirse como parte del texto del mensaje. Solo en circunstancias muy raras, el sistema de mensajería tiene tan poca compatibilidad con las propiedades de mensajes que es necesaria para la codificación TNEF completa de todas las propiedades.
    
- Mecanismo para determinar si una secuencia TNEF en un mensaje entrante pertenece al mensaje, en función de la propiedad MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Esta propiedad debe encontrarse tanto en la secuencia TNEF como en un encabezado de mensaje adecuado. Si la propiedad tiene el mismo valor en ambos lugares, o falta en cualquier lugar, se supone que el flujo TNEF pertenece al mensaje. De lo contrario, se omite la secuencia TNEF. Los transportes habilitados para TNEF son responsables de elegir un valor para esta propiedad en los mensajes salientes y de codificarlo en un encabezado de mensaje apropiado (por ejemplo, el encabezado Message-ID: para los mensajes SMTP) y en la secuencia TNEF.
    

