---
title: Objetos y propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411214"
---
# <a name="mapi-objects-and-properties"></a>Objetos y propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunas propiedades son compatibles con muchos tipos diferentes de objetos. Las siguientes propiedades son ejemplos de propiedades que usan varios objetos:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) es un identificador binario que se usa para abrir objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es una constante usada para identificar el tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es una cadena de caracteres que se usa para describir un objeto al usuario.
    
Otras propiedades tienen sentido para un único tipo de objeto. Las siguientes propiedades son ejemplos de propiedades que se aplican a un tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) es una cadena de caracteres que se usa para describir el tipo de un mensaje.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) es un entero que se usa para identificar una fila de una tabla.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) es un entero que se usa para almacenar el número de bytes en un archivo adjunto.
    
Aún así, otras propiedades solo son aplicables a un único tipo de objeto en un estado determinado. Las propiedades de este tipo suelen ser propiedades de mensaje. Cuando se crea un mensaje por primera vez, su conjunto de propiedades es muy pequeño. A medida que un cliente lo envía a un destinatario a través del sistema de mensajería, aumenta el número de propiedades necesarias para describir el mensaje. Algunas de estas propiedades agregadas aparecen solo en el mensaje mientras se entrega, mientras que otras solo aparecen en el mensaje mientras se envía. Los mensajes también tienen propiedades asociadas a la clase a la que pertenecen. Los mensajes de informe, por ejemplo, tienen propiedades que no son compatibles con los mensajes de otras clases, como los mensajes de nota. 
  
Cada objeto tiene algunas propiedades necesarias y puede o no tener otras propiedades opcionales. Las propiedades necesarias son propiedades que deben existir en un objeto para que el objeto se pueda guardar correctamente con su [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Los clientes o proveedores de servicios que usan un objeto pueden depender de la disponibilidad de las propiedades necesarias después de la **llamada a SaveChanges.** Es decir, pueden estar seguros de que una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) del objeto o al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para recuperar estas propiedades se realizará correctamente. 
  
Las propiedades opcionales son propiedades que, según el implementador del objeto, pueden o no ser compatibles con un objeto. Un cliente o proveedor de servicios que usa el objeto no puede esperar que las propiedades opcionales estén disponibles a través de los **métodos GetProps** o **OpenProperty** y que se establezcan en valores válidos. 
  
Para obtener una lista o propiedades en esta referencia, vea [propiedades MAPI](mapi-properties.md). Las descripciones de las propiedades pertenecientes a cada uno de los objetos del almacén de mensajes y de la libreta de direcciones se pueden encontrar en la descripción de la interfaz estándar del objeto. Por ejemplo, las propiedades de carpeta se analizan **con IMAPIFolder** y las propiedades de usuario de mensajería se analizan con **IMailUser**. Las propiedades del mensaje, incluidas las propiedades del mensaje de informe, se describen **con IMessage** y en [Message Properties Overview](message-properties-overview.md). Las propiedades pertenecientes a cada uno de los distintos tipos de tablas se describen en el tema de [tablas MAPI](mapi-tables.md) correspondiente. Por ejemplo, las propiedades de la tabla de jerarquía se describen en [tablas de jerarquía.](hierarchy-tables.md) Las propiedades pertenecientes a los servidores de formulario se describen [al elegir el conjunto de propiedades de un formulario](choosing-a-form-s-property-set.md).
  
Cuando un cliente o proveedor de servicios llama al método **GetProps** de un objeto para recuperar varias de sus propiedades y una de estas propiedades no está disponible, **GetProps** devuelve la advertencia MAPI_W_ERRORS_RETURNED. La llamada se considera correcta porque se devolvieron algunas de las propiedades. Cuando un cliente o proveedor de servicios llama **a OpenProperty** y la propiedad de destino no está disponible, el método produce el error MAPI_E_NOT_FOUND. Es importante comprobar que se devuelve una propiedad solicitada antes de intentar trabajar con ella. 
  
Según el objeto, el proveedor de servicios que suministra la implementación y la propiedad, una propiedad puede tener permisos de solo lectura/escritura o de solo lectura. El permiso de lectura y escritura permite a un cliente o proveedor de servicios usar la propiedad cambiar su valor; El permiso de solo lectura solo permite que el proveedor de servicios propietario del objeto realice cambios. 
  
Para averiguar exactamente qué propiedades están establecidas actualmente para un objeto, llame a [IMAPIProp::GetPropList](imapiprop-getproplist.md). El **método GetPropList permite** al autor de la llamada averiguar qué está disponible antes de intentar abrir una propiedad potencialmente inexistente. Dado que no hay ningún conjunto estándar de propiedades que admitan todos los objetos de un tipo específico, es imposible adivinar si un objeto admite o no una propiedad determinada. Llamar **a GetPropList** elimina el trabajo de suposición. 
  
## <a name="see-also"></a>Consulte también



[Objetos y propiedades MAPI](mapi-objects-and-properties.md)

