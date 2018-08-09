---
title: Las propiedades y objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0efc111523ad285d54fc40e37fe83a1130f1d291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818161"
---
# <a name="mapi-objects-and-properties"></a>Las propiedades y objetos MAPI

  
  
**Hace referencia a**: Outlook 
  
Algunas propiedades son compatibles con muchos tipos diferentes de objetos. Las propiedades siguientes son ejemplos de propiedades que se usan por varios objetos:
  
- **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) es un identificador binario utilizado para abrir los objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es una constante que se utiliza para identificar el tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es una cadena de caracteres que se usa para describir un objeto al usuario.
    
Otras propiedades que tenga sentido para un único tipo de objeto. Las propiedades siguientes son ejemplos de propiedades que se aplican a un tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) es una cadena de caracteres que se usa para describir el tipo de un mensaje.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) es un entero que se usa para identificar una fila en una tabla.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) es un entero que se usa para almacenar el número de bytes en un archivo adjunto.
    
Aún otras propiedades son aplicables sólo para un único tipo de objeto en un estado determinado. Las propiedades de este tipo suelen ser propiedades del mensaje. Cuando se crea por primera vez un mensaje, su conjunto de propiedades es muy pequeño. Cuando se envía por un cliente a un destinatario mediante el sistema de mensajería, aumenta el número de propiedades necesarias para describir el mensaje. Algunas de estas propiedades se agregaron sólo aparecen en el mensaje como se entregarse mientras que otros usuarios sólo aparecen en el mensaje tal y como se está enviando. Los mensajes también tienen propiedades que están asociadas con la clase a la que pertenecen. Mensajes de informe, por ejemplo, tienen propiedades que no son compatibles con los mensajes de otras clases, como los mensajes de nota. 
  
Cada objeto tiene algunas propiedades necesarias y puede o no tener otras propiedades opcionales. Propiedades necesarias son las propiedades que deben existir en un objeto antes de poder guardar correctamente el objeto con su método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Los clientes o proveedores de servicios de uso de un objeto pueden depender de la disponibilidad de las propiedades necesarias después de la llamada de **SaveChanges** . Es decir, puede estar seguro de que una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) (método) del objeto o el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para recuperar estas propiedades se realizará correctamente. 
  
Propiedades opcionales son propiedades que, dependiendo del implementador del objeto, es posible que o podrán no ser admitidas por un objeto. Un proveedor de servicio o cliente con el objeto no se puede esperar propiedades opcionales estén disponibles a través de los métodos **GetProps** o **OpenProperty** y se establece en los valores válidos. 
  
Para una lista o propiedades en esta referencia, vea [Las propiedades MAPI](mapi-properties.md). Descripciones de propiedades que pertenecen a cada uno de los mensajes de almacenan y objetos de la libreta de direcciones pueden encontrarse en la descripción de la interfaz del objeto estándar. Por ejemplo, propiedades de la carpeta se tratan con **IMAPIFolder** y propiedades de usuario de mensajería se analizan con **IMailUser**. Propiedades del mensaje, incluidas las propiedades de mensaje de informe, se describen con **IMessage** y en [Información general de las propiedades del mensaje](message-properties-overview.md). Las propiedades que pertenecen a cada uno de los diferentes tipos de tablas se describen en el tema correspondiente de [Las tablas de MAPI](mapi-tables.md) . Por ejemplo, las propiedades de la tabla de jerarquía se describen en [Las tablas de jerarquía](hierarchy-tables.md). Las propiedades que pertenecen a los servidores de formulario se que describe la elección de [Propiedad establecida un formulario](choosing-a-form-s-property-set.md).
  
Cuando un proveedor de servicio o cliente llama a un método del objeto **GetProps** para recuperar varias de sus propiedades y una de estas propiedades no está disponible, **GetProps** devuelve la advertencia MAPI_W_ERRORS_RETURNED. La llamada se considera ser correcta, ya que algunas de las propiedades se han devuelto. Cuando un cliente o las llamadas de proveedor de servicio **OpenProperty** y la propiedad de destino no está disponible, el método se produce el error MAPI_E_NOT_FOUND. Es importante comprobar que se devuelve una propiedad solicitada antes de intentar trabajar con él. 
  
Según el objeto, el proveedor de servicios de proporcionar la implementación y la propiedad, una propiedad puede tener permiso de solo lectura o de lectura y escritura. Permiso de lectura y escritura permite a un proveedor de servicio o de cliente mediante la propiedad para cambiar su valor; permiso de sólo lectura permite sólo el proveedor de servicios propietarios del objeto realizar cambios. 
  
Para averiguar exactamente qué propiedades se encuentran actualmente definidas para un objeto, llame a [IMAPIProp::GetPropList](imapiprop-getproplist.md). El método **GetPropList** permite a un autor de la llamada a averiguar qué está disponible antes de que se realiza un intento para abrir una propiedad potencialmente inexistente. Debido a que no hay ningún conjunto estándar de propiedades que admiten todos los objetos de un tipo específico, es imposible adivinar independientemente de si está o no admite una propiedad determinada de un objeto. Al llamar a **GetPropList** , elimina el trabajo de estimación. 
  
## <a name="see-also"></a>Vea también



[Las propiedades y objetos MAPI](mapi-objects-and-properties.md)

