---
title: Desarrollo de un proveedor TNEF-Enabled transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 282b1866699b695c647caedd130ce5abc1bcbc2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439005"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desarrollo de un proveedor TNEF-Enabled transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para promover la interoperabilidad entre sistemas de mensajería que admiten distintos conjuntos de características MAPI, MAPI proporciona el formato de encapsulación neutral de transporte (TNEF) como una forma estándar de transferir datos. Este formato encapsula las propiedades MAPI no admitidas por un sistema de mensajería subyacente en una secuencia binaria que se puede transferir junto con el mensaje cuando un proveedor de transporte lo envía. A continuación, el proveedor de transporte que recibe el mensaje puede descodificar la secuencia binaria para recuperar todas las propiedades del mensaje original y hacerlas disponibles para las aplicaciones cliente. El modelo operativo de TNEF es:
  
- Los clientes de mensajería envían y reciben mensajes a un transporte TNEF de forma normal.
    
- El transporte separa las propiedades de los mensajes salientes en dos categorías: las que admite el sistema de mensajes subyacente y las que no. Los valores de las propiedades admitidas por el sistema de mensajería subyacente se traducen al formato requerido.
    
- El transporte usa los métodos TNEF MAPI para codificar las propiedades no admitidas en un único flujo de datos. A continuación, el transporte convierte esa secuencia de datos en datos adjuntos especiales en el mensaje saliente, mediante el modelo de datos adjuntos del sistema de mensajería subyacente, antes de enviar el mensaje.
    
- Un transporte habilitado para TNEF que recibe un mensaje de este tipo hace dos cosas. En primer lugar, traduce las propiedades del mensaje entrante (las que admite el sistema de mensajes subyacente) en propiedades MAPI. En segundo lugar, si los datos adjuntos especiales están presentes, usa los métodos TNEF MAPI para recuperar propiedades MAPI adicionales de los datos adjuntos antes de entregar el mensaje a una aplicación cliente.
    
MAPI proporciona una implementación de la **interfaz ITnef** para su uso por los proveedores de transporte MAPI al trabajar con objetos TNEF. La [función OpenTnefStreamEx](opentnefstreamex.md) se usa para crear objetos TNEF y asociarlos con un mensaje. Las secuencias TNEF se construyen sobre la interfaz OLE **IStream** 
  
> [!NOTE]
> Use **OpenTnefStreamEx para** crear objetos TNEF. La función **OpenTnefStream** antigua aún existe por compatibilidad con código fuente antiguo y no debe usarse en nada nuevo. 
  
La **interfaz ITnef** proporciona los siguientes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
El modelo de implementación de TNEF MAPI admite:
  
- Todas las propiedades MAPI sin afectar a otras propiedades de mensaje. Para que los mensajes MAPI sobrevivan al transporte a través de un sistema de mensajería, todas las propiedades que no se pueden codificar como propiedades del sistema de mensajería deben encapsularse. Dado que casi nunca se sabe en el momento en que se envía un mensaje si un cliente compatible con MAPI recibirá o no el mensaje, el esquema de encapsulación permite a un proveedor de transporte codificar solo aquellas propiedades de mensaje MAPI que el sistema de mensajería no admite de forma nativa. Esto significa que los mensajes que usan TNEF no son "opacos" para los sistemas de mensajería que no se basan en MAPI, como los sistemas de mensajería UNIX SMTP. Estos sistemas reciben las propiedades que admiten de la forma que sea habitual para ellos y otras propiedades se reciben como una secuencia de datos TNEF codificada. El proveedor de transporte TNEF es responsable de diferenciar entre estos dos conjuntos de propiedades y enviar el conjunto admitido de la manera adecuada para el sistema de mensajería. TNEF no asume el nivel de compatibilidad proporcionado por un sistema de mensajería. Sin embargo, en los ejemplos de uso de TNEF incluidos en esta sección, se supone que el sistema de mensajería admite al menos un único dato adjunto aparte del mensaje. En algunos casos, los datos adjuntos solo pueden ser compatibles a través de una secuencia uuencoded y transmitirse como parte del texto del mensaje. Solo en circunstancias muy raras el sistema de mensajería tendrá tan poca compatibilidad con las propiedades de mensaje que es necesaria la codificación TNEF completa de todas las propiedades.
    
- Mecanismo para determinar si una secuencia TNEF de un mensaje entrante pertenece al mensaje, basado en la propiedad MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Esta propiedad debe encontrarse tanto en la secuencia TNEF como en un encabezado de mensaje adecuado. Si la propiedad tiene el mismo valor en ambos lugares o falta en cualquier lugar, se supone que la secuencia TNEF pertenece al mensaje. De lo contrario, se omite la secuencia TNEF. Los transportes habilitados para TNEF son responsables de elegir un valor para esta propiedad en los mensajes salientes y codificar en un encabezado de mensaje adecuado (por ejemplo, el encabezado Message-ID: para los mensajes SMTP) y en la secuencia TNEF.
    

