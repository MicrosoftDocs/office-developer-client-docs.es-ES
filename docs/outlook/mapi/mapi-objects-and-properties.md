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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345811"
---
# <a name="mapi-objects-and-properties"></a>Objetos y propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunas propiedades son compatibles con muchos tipos de objetos diferentes. Las siguientes propiedades son ejemplos de propiedades que usan varios objetos:
  
- **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md)) es un identificador binario que se usa para abrir objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es una constante usada para identificar el tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es una cadena de caracteres que se usa para describir un objeto al usuario.
    
Otras propiedades tienen sentido para un único tipo de objeto. Las siguientes propiedades son ejemplos de propiedades que se aplican a un tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) es una cadena de caracteres que se usa para describir el tipo de un mensaje.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) es un entero que se usa para identificar una fila en una tabla.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) es un entero que se usa para almacenar el número de bytes en datos adjuntos.
    
Sin embargo, otras propiedades solo son aplicables a un único tipo de objeto en un estado específico. Las propiedades de este tipo suelen ser propiedades de mensaje. Cuando se crea un mensaje por primera vez, su conjunto de propiedades es muy pequeño. A medida que un cliente envía a un destinatario a través del sistema de mensajería, aumenta el número de propiedades necesarias para describir el mensaje. Algunas de estas propiedades agregadas aparecen sólo en el mensaje cuando se entrega mientras que otras aparecen sólo en el mensaje cuando se envía. Los mensajes también tienen propiedades asociadas a la clase a la que pertenecen. Los mensajes de informe, por ejemplo, tienen propiedades que no son compatibles con los mensajes de otras clases, como los mensajes de notas. 
  
Cada objeto tiene algunas propiedades necesarias y puede o no tener otras propiedades opcionales. Las propiedades necesarias son propiedades que deben existir en un objeto antes de que el objeto se pueda guardar correctamente con su método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Los clientes o proveedores de servicios que utilizan un objeto pueden depender de la disponibilidad de las propiedades necesarias después de la llamada a **SaveChanges** . Es decir, puede estar seguro de que se realizará correctamente una llamada al método [IMAPIProp:: GetProps](imapiprop-getprops.md) o [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del objeto para recuperar estas propiedades. 
  
Las propiedades opcionales son propiedades que, según el implementador del objeto, pueden o no ser compatibles con un objeto. Un cliente o proveedor de servicios que usa el objeto no puede esperar que las propiedades opcionales estén disponibles a través de los métodos **GetProps** o **OpenProperty** y se establezcan en valores válidos. 
  
Para obtener una lista o propiedades en esta referencia, consulte [MAPI Properties](mapi-properties.md). Puede encontrar deScripciones de las propiedades que pertenecen a cada uno de los objetos de almacén de mensajes y de la libreta de direcciones en la descripción de la interfaz estándar del objeto. Por ejemplo, las propiedades de la carpeta se explican con **IMAPIFolder** y las propiedades de usuario de mensajería se describen con **IMailUser**. Las propiedades de los mensajes, incluidas las propiedades de los mensajes de informe, se describen con **IMessage** y en [información general de las propiedades del mensaje](message-properties-overview.md). Las propiedades que pertenecen a cada uno de los distintos tipos de tablas se describen en el tema [tablas MAPI](mapi-tables.md) apropiadas. Por ejemplo, las propiedades de la tabla de jerarquía se describen en [tablas de jerarquía](hierarchy-tables.md). Las propiedades que pertenecen a los servidores de formularios se describen en [elegir el conjunto de propiedades de un formulario](choosing-a-form-s-property-set.md).
  
Cuando un cliente o proveedor de servicios llama al método **GetProps** de un objeto para recuperar varias de sus propiedades y una de estas propiedades no está disponible, **GetProps** devuelve la advertencia MAPI_W_ERRORS_RETURNED. Se considera que la llamada es correcta porque se han devuelto algunas propiedades. Cuando un cliente o proveedor de servicios llama a **OpenProperty** y la propiedad de destino no está disponible, el método produce el error MAPI_E_NOT_FOUND. Es importante comprobar que se devuelve una propiedad solicitada antes de intentar trabajar con ella. 
  
Dependiendo del objeto, el proveedor de servicios que proporciona la implementación y la propiedad, una propiedad puede tener permiso de lectura y escritura o de solo lectura. Permiso de lectura y escritura permite a un proveedor de servicios o cliente que usa la propiedad cambiar su valor; permiso de solo lectura permite que solo el proveedor de servicios propietario del objeto realice cambios. 
  
Para averiguar exactamente qué propiedades están establecidas actualmente para un objeto, llame a [IMAPIProp:: GetPropList](imapiprop-getproplist.md). El método **GetPropList** permite al autor de la llamada averiguar qué hay disponible antes de que se intente abrir una propiedad potencialmente no existente. Dado que no hay ningún conjunto estándar de propiedades que admitan todos los objetos de un tipo específico, es imposible adivinar si un objeto admite o no una propiedad determinada. Llamar a **GetPropList** elimina el trabajo de conjeturas. 
  
## <a name="see-also"></a>Vea también



[Objetos y propiedades MAPI](mapi-objects-and-properties.md)

