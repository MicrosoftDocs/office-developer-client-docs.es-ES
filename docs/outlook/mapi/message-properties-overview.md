---
title: Información general de propiedades de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78e2f63746a866603bc2392fbe5c8bb25d3f38c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818395"
---
# <a name="message-properties-overview"></a>Información general de propiedades de mensaje

  
  
**Hace referencia a**: Outlook 
  
MAPI divide en tres tipos de propiedades del mensaje:
  
- Propiedades de contenido del mensaje.
    
- Propiedades de transmisión, o un sobre del mensaje.
    
- Propiedades de destinatario del mensaje.
    
Propiedades de contenido del mensaje describen el texto de un mensaje. Cada clase de mensaje tiene su propio conjunto de propiedades de contenido. MAPI define las propiedades de contenido para los mensajes de nota y el informe; depende de los clientes y los proveedores de almacén de mensajes que controlan estas clases de mensajes para establecer las propiedades de forma adecuada para sus implementaciones. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) son ejemplos de propiedades de contenido para los mensajes de nota. **PR_BODY** contiene el contenido sin formato de una nota, mientras que **PR_RTF_COMPRESSED** contiene la versión comprimida de contenido con formato de la nota. Para obtener más información acerca de intervalos de identificador de propiedad, vea [Intervalos de identificador de propiedad](property-identifier-ranges.md).
  
Para nuevas clases de mensaje, los clientes pueden definir las propiedades específicas del contenido de una de dos maneras:
  
- Mediante el uso de identificadores de propiedad en el intervalo de propiedades de contenido de clase de mensaje personalizado: 0x6800 a través de 0x7BFF.
    
- Mediante el uso de las propiedades que tienen identificadores que se dividen en el 0 x 8000 a través de 0xFFFE rango con nombre.
    
El intervalo de identificadores de las propiedades de contenido de clase de mensaje personalizado está disponible para cualquier cliente que crea una clase de mensaje personalizada. Por lo tanto, se puede usar un identificador de la propiedad en este intervalo para varias clases de mensaje. Los usuarios de las propiedades de este intervalo no pueden realizar suposiciones sobre el comportamiento de las propiedades. 
  
Para las propiedades con nombre, los clientes de creación un nombre que especifica un conjunto de propiedades y una cadena de caracteres o un valor numérico para cada nueva propiedad. Los clientes, a continuación, asociación la propiedad con un identificador en el intervalo de la propiedad con nombre. Los usuarios de propiedades con nombre acceso a ellos por nombre o identificador a través de los métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) . 
  
Las propiedades del contenedor proporcionan información que se usa para transmitir un mensaje de un destinatario a otra. Al igual que con las propiedades de contenido de mensaje, es posible para los clientes o proveedores de servicios definir sus propios las propiedades del contenedor complementarlas que define de MAPI. Los clientes y los proveedores de transporte establecen las propiedades de sobres que define MAPI en función de la definición de MAPI. Los proveedores de transporte que implementen las características especiales pueden definir sus propios las propiedades del contenedor para exponer esas características a los clientes. MAPI reservar establece un intervalo de identificadores de las propiedades que se pueden usar para estas propiedades definidas por el proveedor especiales. Los proveedores de transporte normalmente implementan una página de propiedades especiales para mostrar estas propiedades y que los clientes puedan modificarlos. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) son ejemplos de las propiedades del contenedor. Para obtener más información, vea [Intervalos de identificador de propiedad](property-identifier-ranges.md).
  
Las propiedades de destinatarios describen el destino de un mensaje enviado. Un destinatario puede ser un usuario de mensajería, lista de distribución o un equipo. Las propiedades de destinatarios se definen mediante MAPI y establecidas por los proveedores de servicios. Algunas propiedades de destinatario son compatibles con los proveedores de la libreta de direcciones para el usuario de mensajería y de objetos de la lista de distribución; otras propiedades de destinatario son compatibles con los clientes, los proveedores de almacén de mensajes o los proveedores de transporte. Por ejemplo, todos los destinatarios requieren una dirección y un tipo de dirección; Estos son mantenidas por un proveedor de la libreta de direcciones cuando el destinatario está almacenado en una de sus contenedores de propiedades. Los destinatarios también tienen un tipo, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), que identifica a un destinatario como una primaria, copia o destinatarios con copia oculta.
  
Muchas propiedades del mensaje son opcionales, lo que significa que los clientes no se prevé que van a estar disponible o se establece a los valores válidos. Algunas propiedades de mensajes son necesarios pero están disponibles únicamente cuando un mensaje está en un estado determinado. Por ejemplo, no se requiere tener un identificador de entrada hasta después de que el mensaje se ha guardado, y no es necesario tener una clase de mensaje hasta que el mensaje está listo para ser enviado un mensaje recién creado. Los clientes siempre deben comprobar los resultados de sus llamadas [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y tienen valores predeterminados listos como una copia de seguridad en caso de una propiedad solicitada no está disponible. 
  
Mayoría de las propiedades de mensaje que establecen los proveedores de servicios es de solo lectura a los clientes. 
  
## <a name="see-also"></a>Vea también



[Mensajes MAPI](mapi-messages.md)

