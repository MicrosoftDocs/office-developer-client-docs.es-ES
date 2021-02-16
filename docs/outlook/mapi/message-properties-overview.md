---
title: Introducción a las propiedades del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 515b4637f99b806c5c5bc6304f107f62ca6d9091
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420251"
---
# <a name="message-properties-overview"></a>Introducción a las propiedades del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI divide las propiedades del mensaje en tres tipos:
  
- Propiedades del contenido del mensaje.
    
- Propiedades de transmisión de mensajes o sobre.
    
- Propiedades del destinatario del mensaje.
    
Las propiedades de contenido del mensaje describen el texto de un mensaje. Cada clase de mensaje tiene su propio conjunto de propiedades de contenido. MAPI define las propiedades de contenido para los mensajes de nota e informe; corresponde a los clientes y proveedores de almacén de mensajes que controlan estas clases de mensajes establecer las propiedades adecuadamente para sus implementaciones. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) son ejemplos de propiedades de contenido para los mensajes de nota. **PR_BODY** contiene el contenido sin formato de una nota, mientras que **PR_RTF_COMPRESSED** contiene la versión comprimida del contenido con formato de una nota. Para obtener más información acerca de los intervalos de identificadores de propiedad, vea [Intervalos de identificadores de propiedad.](property-identifier-ranges.md)
  
Para las nuevas clases de mensajes, los clientes pueden definir propiedades específicas del contenido de una de estas dos maneras:
  
- Mediante el uso de identificadores de propiedad en el intervalo de propiedades de contenido de clase de mensaje personalizado: 0x6800 a 0x7BFF.
    
- Mediante el uso de propiedades con nombre que tienen identificadores que se 0x8000 a través 0xFFFE rango.
    
El intervalo de identificadores de las propiedades de contenido de clase de mensaje personalizadas está disponible para cualquier cliente que cree una clase de mensaje personalizada. Por lo tanto, se puede usar un identificador de propiedad en este intervalo para varias clases de mensajes. Los usuarios de propiedades de este intervalo no pueden hacer suposiciones sobre el comportamiento de las propiedades. 
  
Para las propiedades con nombre, los clientes crean un nombre que especifica un conjunto de propiedades y una cadena de caracteres o un valor numérico para cada nueva propiedad. A continuación, los clientes asocian la propiedad con un identificador en el intervalo de propiedades con nombre. Los usuarios de propiedades con nombre tienen acceso a ellas por nombre o identificador a través de los métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md) 
  
Las propiedades de sobre proporcionan información que se usa para transmitir un mensaje de un destinatario a otro. Al igual que con las propiedades de contenido de mensajes, es posible que los clientes o proveedores de servicios definan sus propias propiedades de sobre para complementar las que define MAPI. Los clientes y proveedores de transporte establecen las propiedades de sobre que MAPI define en función de la definición que proporciona MAPI. Los proveedores de transporte que implementan características especiales pueden definir sus propias propiedades de sobre para exponer dichas características a los clientes. MAPI reserva un intervalo de identificadores de propiedad que se pueden usar para estas propiedades especiales definidas por el proveedor. Normalmente, los proveedores de transporte implementan una página de propiedades especial para mostrar estas propiedades y permitir que los clientes las cambien. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) son ejemplos de propiedades de sobre. Para obtener más información, vea [Intervalos de identificadores de propiedad.](property-identifier-ranges.md)
  
Las propiedades de destinatario describen el destino de un mensaje enviado. Un destinatario puede ser un usuario de mensajería, una lista de distribución o un equipo. Las propiedades de destinatario se definen mediante MAPI y las establecen los proveedores de servicios. Algunas propiedades de destinatario son compatibles con los proveedores de libretas de direcciones para sus objetos de lista de distribución y usuario de mensajería; Otras propiedades de destinatario son compatibles con clientes, proveedores de al almacenamiento de mensajes o proveedores de transporte. Por ejemplo, todos los destinatarios requieren una dirección y un tipo de dirección; estas son propiedades mantenidas por un proveedor de libreta de direcciones cuando el destinatario se almacena en uno de sus contenedores. Los destinatarios también tienen un tipo, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), que identifica a un destinatario como destinatario principal, de copia carbón o de copia carbón.
  
Muchas propiedades de mensaje son opcionales, lo que significa que los clientes no pueden esperar que estén disponibles o establecidas en valores válidos. Algunas propiedades del mensaje son necesarias pero solo están disponibles cuando un mensaje está en un estado determinado. Por ejemplo, no es necesario que un mensaje recién creado tenga un identificador de entrada hasta que se haya guardado el mensaje y no es necesario tener una clase de mensaje hasta que el mensaje esté listo para enviarse. Los clientes siempre deben comprobar los resultados de sus llamadas [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y tener los valores predeterminados listos como copia de seguridad en caso de que una propiedad solicitada no esté disponible. 
  
La mayoría de las propiedades de mensaje que establecen los proveedores de servicios son de solo lectura para los clientes. 
  
## <a name="see-also"></a>Consulte también



[Mensajes MAPI](mapi-messages.md)

