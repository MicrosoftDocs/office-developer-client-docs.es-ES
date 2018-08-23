---
title: Propiedad canónica PidTagMessageFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8082b0b6d47a16a79f5e426375e20b17d22298d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586623"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propiedad canónica PidTagMessageFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcadores que indican el origen y el estado actual de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificador:  <br/> |0x0E07  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una propiedad de mensaje nontransmittable expuesta en el envío y recepción de extremos de una transmisión, con valores diferentes dependiendo del proveedor de almacén o de la aplicación de cliente necesarios para. Esta propiedad se inicializa por el proveedor de almacén de cliente o un mensaje cuando se crea un mensaje y se guarda por primera vez y, a continuación, actualiza periódicamente por el proveedor de almacenamiento de mensajes, un proveedor de transporte y la cola MAPI tal y como se procesa el mensaje y su estado cambios. 
  
Esta propiedad existe en un mensaje antes y después de la presentación y en todas las copias del mensaje recibido. Aunque no es una propiedad de destinatario, se exponen de manera diferente para cada destinatario en función de si se ha leído o modificados por ese destinatario. 
  
Esta propiedad se pueden establecer uno o varios de los siguientes indicadores:
  
MSGFLAG_ASSOCIATED 
  
> El mensaje es un mensaje de una carpeta asociado. El cliente o el proveedor tiene acceso de solo lectura para esta marca. El indicador MSGFLAG_READ se omite para los mensajes asociados, que no conservan un estado leído o no leído. 
    
MSGFLAG_FROMME 
  
> El envío de usuario mensajería fue el usuario de mensajería recibe el mensaje. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de sólo lectura a partir de entonces. Esta marca está pensada para ser establecidos por el proveedor de transporte. 
    
MSGFLAG_HASATTACH 
  
> El mensaje tiene al menos un dato adjunto. Esta marca corresponde a la propiedad del mensaje **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)). El cliente tiene acceso a esta marca de solo lectura. 
    
MSGFLAG_NRN_PENDING 
  
> Un informe nonread debe enviarse para el mensaje. El cliente o el proveedor tiene acceso de solo lectura para esta marca. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> El mensaje entrante ha llegado a través de Internet. Se ha originado fuera de la organización o desde un origen que no se puede tener en cuenta la puerta de enlace de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> El mensaje entrante ha llegado a través de un vínculo externo que no sea X.400 o de Internet. Se ha originado fuera de la organización o desde un origen que no se puede tener en cuenta la puerta de enlace de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_X400 
  
> El mensaje entrante ha llegado a través de un vínculo X.400. Se ha originado fuera de la organización o desde un origen que no se puede tener en cuenta la puerta de enlace de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_READ 
  
> El mensaje está marcado como leídos. Esto puede ocurrir como resultado de una llamada en cualquier momento a [IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Los clientes también pueden establecer esta marca mediante una llamada al método de **IMAPIProp::SetProps** de un mensaje antes de que el mensaje se ha guardado por primera vez. Este indicador se omite si se establece la marca **MSGFLAG_ASSOCIATED** . 
    
MSGFLAG_RESEND 
  
> El mensaje incluye una solicitud para una operación de volver a enviar con un informe de no entrega. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de sólo lectura a partir de entonces. 
    
MSGFLAG_RN_PENDING 
  
> Un informe de lectura debe enviarse para el mensaje. El cliente o el proveedor tiene acceso de solo lectura para esta marca. 
    
MSGFLAG_SUBMIT 
  
> El mensaje está marcado para el envío como resultado de una llamada a [IMessage::SubmitMessage](imessage-submitmessage.md). Los proveedores de almacén de mensajes establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_UNMODIFIED 
  
> El mensaje saliente no se ha modificado desde la primera vez que se guardó; el mensaje entrante no se ha modificado desde que se entregó. 
    
MSGFLAG_UNSENT 
  
> Aún se está compuesta por el mensaje. Se guarda, pero no se ha enviado. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de sólo lectura a partir de entonces. Si un cliente no establezca esta marca en el momento en que se envía el mensaje, el proveedor de almacén de mensajes establece cuando se llama a **IMessage::SubmitMessage** . Normalmente, esta marca está desactivada después de que el mensaje se envía. 
    
Un proveedor de almacén de cliente o un mensaje puede comprobar el estado actual del mensaje en cualquier momento llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) para leer los valores de indicador. El cliente o el proveedor también puede llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) para cambiar los indicadores que actualmente tienen acceso de lectura y escritura. 
  
Varias de las marcas son siempre de sólo lectura. Algunas son de lectura y escritura hasta que la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y posteriormente se convierten en solo lectura en lo que se refiere a **IMAPIProp::SetProps** . Uno de los siguientes, MSGFLAG_READ, se puede cambiar más adelante a través de [IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Normalmente, los valores iniciales para esta propiedad son MSGFLAG_UNSENT y MSGFLAG_UNMODIFIED para indicar un mensaje que aún no se han enviado o se ha cambiado. Cuando se guarda un mensaje por segunda vez, el proveedor de almacenamiento de mensaje borra el indicador MSGFLAG_UNMODIFIED. Otro valor que puede establecer un proveedor de almacén de mensajes cuando se guarda un mensaje es la marca MSGFLAG_HASATTACH, que indica que el mensaje tiene uno o más datos adjuntos. La propiedad **PR_HASATTACH** se calcula a partir de esta configuración. 
  
Cuando un cliente llama al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje, el proveedor de almacén de mensajes realiza una copia de la misma para la cola MAPI y actualiza esta propiedad estableciendo el indicador MSGFLAG_SUBMIT. El proveedor de almacén de mensajes también establece MSGFLAG_UNSENT si no está establecido todavía. MSGFLAG_SUBMIT indica que se ha llamado **SubmitMessage** , iniciar el proceso de envío, y que el mensaje es ahora de sólo lectura para el cliente. MSGFLAG_UNSENT indica que el mensaje encarga de la cola de MAPI. Si se cancela el proceso de envío, el proveedor de almacenamiento de mensaje restablece esta marca. 
  
Cuando el mensaje se concede a un proveedor de transporte para la entrega, el proveedor de transporte establece la marca MSGFLAG_FROMME si el remitente tenía la misma cuenta en el servidor de mensajería, como el mensaje se recibió en. Los proveedores de transporte establecen MSGFLAG_FROMME para un mensaje entrante que se ha enviado por el usuario ha iniciado sesión actualmente. Un cliente puede usar este valor para determinar que es más adecuado mostrar los nombres de los destinatarios en la tabla de contenido de la carpeta Elementos enviados de nombres de los remitentes. También deben mostrarse los mensajes que se han guardado durante el proceso de composición y aún no se ha enviado con los nombres de los destinatarios en lugar de nombres de los remitentes. 
  
Para un mensaje entrante, un proveedor de almacén de mensajes borra el indicador MSGFLAG_READ para restablecer su estado de lectura. Un cliente puede establecer o borrar la marca MSGFLAG_READ cuando sea necesario cambiar el estado de lectura y controlar el envío de informes de lectura y nonread, mediante una llamada al método [IMessage::SetReadFlag](imessage-setreadflag.md) del mensaje o en su carpeta [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) (método). La diferencia principal entre estos métodos, que no sea el objeto implementarlos, es que el método de la carpeta puede afectar a uno, varios o todos los mensajes en la carpeta. El método mensaje afecta a un solo mensaje. 
  
Un cliente también debe probar un mensaje entrante para los indicadores MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET y MSGFLAG_ORIGIN_MISC_EXT. Estas marcas se han establecido por el proveedor de transporte de entrada e indican que el mensaje llegó desde un origen que no se puede tener en cuenta la puerta de enlace de confianza. Esto significa que el mensaje originó fuera de la organización, o internamente pero desde una estación de trabajo no sabe que la puerta de enlace. En cualquier caso, no se puede confirmar la identidad del remitente y hay un riesgo de introducir un virus de equipo en la organización. El cliente debe mostrar un mensaje de advertencia al usuario y ofrecer una opción de eliminar el mensaje sin abrirlo. 
  
Los proveedores de almacén de mensajes establecen la marca MSGFLAG_UNMODIFIED para los mensajes entrantes. MSGFLAG_UNMODIFIED indica que un mensaje no se ha cambiado con respecto a la entrega. Un cliente no puede borrar este valor después de que se ha establecido por un proveedor de almacén de mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

