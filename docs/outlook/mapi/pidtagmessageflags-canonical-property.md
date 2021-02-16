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
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325748"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propiedad canónica PidTagMessageFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que indican el origen y el estado actual de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificador:  <br/> |0x0E07  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una propiedad de mensaje notransmitible expuesta en los extremos de envío y recepción de una transmisión, con valores diferentes según la aplicación cliente o el proveedor de almacén implicado. Esta propiedad la inicializa el cliente o el proveedor del almacén de mensajes cuando se crea y se guarda un mensaje por primera vez y, a continuación, se actualiza periódicamente por el proveedor de al almacenamiento de mensajes, un proveedor de transporte y la cola MAPI a medida que se procesa el mensaje y su estado cambia. 
  
Esta propiedad existe en un mensaje antes y después del envío y en todas las copias del mensaje recibido. Aunque no es una propiedad de destinatario, se expone de forma diferente a cada destinatario en función de si ese destinatario la ha leído o modificado. 
  
Se pueden establecer una o varias de las siguientes marcas para esta propiedad:
  
MSGFLAG_ASSOCIATED 
  
> El mensaje es un mensaje asociado de una carpeta. El cliente o el proveedor tiene acceso de solo lectura a esta marca. La MSGFLAG_READ se omite para los mensajes asociados, que no conservan un estado de lectura/no leído. 
    
MSGFLAG_FROMME 
  
> El usuario de mensajería que envía era el usuario de mensajería que recibía el mensaje. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de entonces. Esta marca está pensada para que la establezca el proveedor de transporte. 
    
MSGFLAG_HASATTACH 
  
> El mensaje tiene al menos un dato adjunto. Esta marca corresponde a la propiedad PR_HASATTACH **del** mensaje ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)). El cliente tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_NRN_PENDING 
  
> Debe enviarse un informe no leído para el mensaje. El cliente o el proveedor tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> El mensaje entrante llegó a través de Internet. Se originó fuera de la organización o desde un origen que la puerta de enlace no puede considerar de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> El mensaje entrante llegó a través de un vínculo externo distinto de X.400 o Internet. Se originó fuera de la organización o desde un origen que la puerta de enlace no puede considerar de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_X400 
  
> El mensaje entrante llegó a través de un vínculo X.400. Se originó fuera de la organización o desde un origen que la puerta de enlace no puede considerar de confianza. El cliente debe mostrar un mensaje adecuado al usuario. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_READ 
  
> El mensaje se marca como leído. Esto puede ocurrir como resultado de una llamada en cualquier momento a [IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Los clientes también pueden establecer esta marca llamando al método **IMAPIProp::SetProps** de un mensaje antes de que el mensaje se haya guardado por primera vez. Esta marca se omite si se **MSGFLAG_ASSOCIATED** marca de destino. 
    
MSGFLAG_RESEND 
  
> El mensaje incluye una solicitud para una operación de reenvía con un informe de no entrega. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de entonces. 
    
MSGFLAG_RN_PENDING 
  
> Es necesario enviar un informe de lectura para el mensaje. El cliente o el proveedor tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_SUBMIT 
  
> El mensaje se marca para enviar como resultado de una llamada a [IMessage::SubmitMessage](imessage-submitmessage.md). Los proveedores de al almacenamiento de mensajes establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_UNMODIFIED 
  
> El mensaje saliente no se ha modificado desde la primera vez que se guardó; el mensaje entrante no se ha modificado desde que se entregó. 
    
MSGFLAG_UNSENT 
  
> El mensaje aún se está componenndo. Se guarda, pero no se ha enviado. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de entonces. Si un cliente no establece esta marca en el momento en que se envía el mensaje, el proveedor del almacén de mensajes lo establece cuando se llama a **IMessage::SubmitMessage.** Normalmente, esta marca se borra después de enviar el mensaje. 
    
Un proveedor de almacenamiento de mensajes o cliente puede comprobar el estado actual del mensaje en cualquier momento llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) para leer los valores de la marca. El cliente o proveedor también puede llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) para cambiar las marcas que actualmente tienen acceso de lectura y escritura. 
  
Varias de las marcas son siempre de solo lectura. Algunos son de lectura y escritura hasta la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y, a partir de entonces, se convierten en solo lectura en lo que respecta a **IMAPIProp::SetProps.** Una de estas opciones, MSGFLAG_READ, se puede cambiar más adelante a través de [IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Los valores iniciales de esta propiedad se suelen MSGFLAG_UNSENT y MSGFLAG_UNMODIFIED para indicar un mensaje que aún no se ha enviado o modificado. Cuando se guarda un mensaje por segunda vez, el proveedor de al almacenamiento de mensajes borra la MSGFLAG_UNMODIFIED mensaje. Otro valor que un proveedor de almacenamiento de mensajes puede establecer cuando se guarda un mensaje es la marca MSGFLAG_HASATTACH, que indica que el mensaje tiene uno o más datos adjuntos. La **PR_HASATTACH** propiedad se calcula a partir de esta configuración. 
  
Cuando un cliente llama al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje, el proveedor del almacén de mensajes hace una copia del mismo para la cola MAPI y actualiza esta propiedad estableciendo la marca MSGFLAG_SUBMIT mensaje. El proveedor de almacenamiento de mensajes también MSGFLAG_UNSENT si aún no está establecido. MSGFLAG_SUBMIT indica que se ha llamado **a SubmitMessage,** comenzando el proceso de envío, y que el mensaje ahora es de solo lectura para el cliente. MSGFLAG_UNSENT indica que la cola MAPI está controlando el mensaje. Si se cancela el proceso de envío, el proveedor del almacén de mensajes restablece esta marca. 
  
Cuando el mensaje se entrega a un proveedor de transporte para su entrega, el proveedor de transporte establece la marca MSGFLAG_FROMME si el remitente tenía la misma cuenta en el servidor de mensajería en el que se recibió el mensaje. Los proveedores de transporte MSGFLAG_FROMME para un mensaje entrante enviado por el usuario que ha iniciado sesión. Un cliente puede usar este valor para determinar que es más apropiado mostrar nombres de destinatarios en la tabla de contenido de la carpeta Elementos enviados que nombres de remitentes. Los mensajes que se han guardado durante el proceso de composición y que aún no se han enviado también deben mostrarse con nombres de destinatarios en lugar de con nombres de remitentes. 
  
Para un mensaje entrante, un proveedor de almacén de mensajes borra MSGFLAG_READ marca para restablecer su estado de lectura. Un cliente puede establecer o borrar la marca MSGFLAG_READ cuando sea necesario cambiar el estado de lectura y controlar el envío de informes leídos y no leídos, llamando al método [IMessage::SetReadFlag](imessage-setreadflag.md) del mensaje o al método [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) de su carpeta. La principal diferencia entre estos métodos, aparte del objeto que los implementa, es que el método de carpeta puede afectar a uno, varios o todos los mensajes de la carpeta. El método de mensaje afecta a un único mensaje. 
  
Un cliente también debe probar un mensaje entrante para las marcas MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET y MSGFLAG_ORIGIN_MISC_EXT entrantes. Estas marcas las establece el proveedor de transporte de entrada e indican que el mensaje llegó desde un origen que la puerta de enlace no puede considerar de confianza. Esto significa que el mensaje se originó fuera de la organización o internamente, pero desde una estación de trabajo que la puerta de enlace no conoce. En cualquier caso, es posible que no se confirme la identidad del remitente y existe el riesgo de introducir un virus informático en la organización. El cliente debe mostrar un mensaje de advertencia al usuario y ofrecer la opción de eliminar el mensaje sin abrirlo. 
  
Los proveedores de al almacenamiento de mensajes MSGFLAG_UNMODIFIED marca para los mensajes entrantes. MSGFLAG_UNMODIFIED indica que no se ha cambiado un mensaje desde la entrega. Un cliente no puede borrar este valor después de que lo haya establecido un proveedor de almacenamiento de mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

