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
  
Contiene una máscara de máscara de marcas que indican el origen y el estado actual de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificador:  <br/> |0x0E07  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una propiedad de mensaje no transmitible expuesta en los extremos de envío y recepción de una transmisión, con valores diferentes según la aplicación cliente o el proveedor de almacenamiento implicado. El cliente o el proveedor del almacén de mensajes inicializa esta propiedad cuando se crea y se guarda un mensaje por primera vez y, a continuación, se actualiza periódicamente por el proveedor de almacenamiento de mensajes, un proveedor de transporte y la cola de espera MAPI cuando se procesa el mensaje y su estado modificación. 
  
Esta propiedad existe en un mensaje antes y después de la entrega, y en todas las copias del mensaje recibido. Aunque no es una propiedad de destinatario, se expone de manera diferente a cada destinatario en función de si el destinatario lo ha leído o modificado. 
  
Se pueden establecer uno o varios de los siguientes indicadores para esta propiedad:
  
MSGFLAG_ASSOCIATED 
  
> El mensaje es un mensaje asociado de una carpeta. El cliente o el proveedor tiene acceso de solo lectura a esta marca. La marca MSGFLAG_READ se ignora para los mensajes asociados, que no conservan el estado de lectura/escritura. 
    
MSGFLAG_FROMME 
  
> El usuario de mensajería que envía es el usuario de mensajería que recibe el mensaje. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de ese momento. Esta marca está pensada para que la establezca el proveedor de transporte. 
    
MSGFLAG_HASATTACH 
  
> El mensaje tiene al menos un archivo de datos adjuntos. Este indicador corresponde a la propiedad **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) del mensaje. El cliente tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_NRN_PENDING 
  
> Es necesario enviar un informe no leído del mensaje. El cliente o el proveedor tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> El mensaje entrante llegó a través de Internet. Se originó fuera de la organización o desde un origen la puerta de enlace no puede considerar de confianza. El cliente debe mostrar al usuario un mensaje apropiado. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> El mensaje entrante llegó a través de un vínculo externo que no sea X. 400 ni de Internet. Se originó fuera de la organización o desde un origen la puerta de enlace no puede considerar de confianza. El cliente debe mostrar al usuario un mensaje apropiado. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_ORIGIN_X400 
  
> El mensaje entrante llegó a través de un vínculo X. 400. Se originó fuera de la organización o desde un origen la puerta de enlace no puede considerar de confianza. El cliente debe mostrar al usuario un mensaje apropiado. Los proveedores de transporte establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_READ 
  
> El mensaje se marca como leído. Esto puede ocurrir como resultado de una llamada en cualquier momento a [IMessage:: SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). Los clientes también pueden establecer esta marca llamando al método **IMAPIProp:: SetProps** del mensaje antes de que el mensaje se haya guardado por primera vez. Esta marca se pasa por alto si se establece la marca **MSGFLAG_ASSOCIATED** . 
    
MSGFLAG_RESEND 
  
> El mensaje incluye una solicitud para una operación de reenvío con un informe de no entrega. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de ese momento. 
    
MSGFLAG_RN_PENDING 
  
> Es necesario enviar un informe de lectura para el mensaje. El cliente o el proveedor tiene acceso de solo lectura a esta marca. 
    
MSGFLAG_SUBMIT 
  
> El mensaje se marca para su envío como resultado de una llamada a [IMessage:: SubmitMessage](imessage-submitmessage.md). Los proveedores de almacenamiento de mensajes establecen esta marca; el cliente tiene acceso de solo lectura. 
    
MSGFLAG_UNMODIFIED 
  
> El mensaje saliente no se ha modificado desde la primera vez que se guardó; el mensaje entrante no se ha modificado desde que se entregó. 
    
MSGFLAG_UNSENT 
  
> El mensaje todavía se está redactando. Se guarda pero no se ha enviado. El cliente o el proveedor tiene acceso de lectura y escritura a esta marca hasta la primera llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y de solo lectura a partir de ese momento. Si un cliente no establece esta marca por el momento en que se envía el mensaje, el proveedor de almacén de mensajes lo establece cuando se llama a **IMessage:: SubmitMessage** . Normalmente, esta marca se borra después de que se envía el mensaje. 
    
Un cliente o un proveedor de almacenamiento de mensajes puede comprobar el estado actual del mensaje en cualquier momento llamando al método [IMAPIProp:: GetProps](imapiprop-getprops.md) para leer los valores de marca. El cliente o el proveedor también puede llamar al método [IMAPIProp:: SetProps](imapiprop-setprops.md) para cambiar cualquier marcador que actualmente tenga acceso de lectura y escritura. 
  
Algunos de los marcadores son siempre de solo lectura. Algunos son de lectura y escritura hasta la primera llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y, a continuación, se convierten en de solo lectura en relación con **IMAPIProp:: SetProps** . Una de ellas, MSGFLAG_READ, se puede cambiar más adelante mediante [IMessage:: SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). 
  
Los valores iniciales de esta propiedad suelen ser MSGFLAG_UNSENT y MSGFLAG_UNMODIFIED para indicar un mensaje que todavía no se ha enviado ni cambiado. Cuando se guarda un mensaje por segunda vez, el proveedor de almacenamiento de mensajes borra la marca MSGFLAG_UNMODIFIED. Otro valor que puede establecer un proveedor de almacén de mensajes cuando se guarda un mensaje es la marca MSGFLAG_HASATTACH, que indica que el mensaje tiene uno o más datos adjuntos. La propiedad **PR_HASATTACH** se calcula a partir de esta configuración. 
  
Cuando un cliente llama al método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar el mensaje, el proveedor de almacenamiento de mensajes crea una copia del mismo para la cola MAPI y actualiza esta propiedad estableciendo la marca MSGFLAG_SUBMIT. El proveedor de almacenamiento de mensajes también establece MSGFLAG_UNSENT si aún no se ha establecido. MSGFLAG_SUBMIT indica que se ha llamado a **SubmitMessage** , comenzando el proceso de envío y que el mensaje ahora es de solo lectura para el cliente. MSGFLAG_UNSENT indica que la cola MAPI está controlando el mensaje. Si se cancela el proceso de envío, el proveedor de almacenamiento de mensajes restablece esta marca. 
  
Cuando el mensaje se entrega a un proveedor de transporte para su entrega, el proveedor de transporte establece la marca MSGFLAG_FROMME si el remitente tiene la misma cuenta en el servidor de mensajería que el mensaje que se recibió. Los proveedores de transporte establecen MSGFLAG_FROMME para un mensaje entrante enviado por el usuario actualmente conectado. Un cliente puede usar este valor para determinar que es más apropiado mostrar los nombres de los destinatarios en la tabla contenido de la carpeta elementos enviados que los nombres del remitente. Los mensajes que se han guardado durante el proceso de composición y todavía no se han enviado deben mostrarse con los nombres de los destinatarios en lugar de los nombres de remitente. 
  
Para un mensaje entrante, un proveedor de almacenamiento de mensajes borra la marca MSGFLAG_READ para restablecer su estado de lectura. Un cliente puede establecer o borrar la marca MSGFLAG_READ cuando es necesario cambiar el estado de lectura y controlar el envío de los informes leídos y no leídos, llamando al método [IMessage:: SetReadFlag](imessage-setreadflag.md) del mensaje o a IMAPIFolder de la carpeta [:: Método SetReadFlags](imapifolder-setreadflags.md) . La diferencia principal entre estos métodos, aparte del objeto que los implementa, es que el método de carpeta puede afectar a uno, varios o todos los mensajes de la carpeta. El método Message afecta a un solo mensaje. 
  
Un cliente también debe probar un mensaje entrante para los indicadores MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET y MSGFLAG_ORIGIN_MISC_EXT. El proveedor de transporte de entrada establece estas marcas e indica que el mensaje llegó desde un origen que la puerta de enlace no puede considerar de confianza. Esto significa que el mensaje se originó fuera de la organización, o bien de forma interna, pero desde una estación de trabajo no conocida para la puerta de enlace. En cualquier caso, la identidad del remitente no se puede confirmar y existe el riesgo de introducir un virus informático en la organización. El cliente debe mostrar un mensaje de advertencia al usuario y ofrece la opción de eliminar el mensaje sin abrirlo. 
  
Los proveedores de almacenamiento de mensajes establecen la marca MSGFLAG_UNMODIFIED para los mensajes entrantes. MSGFLAG_UNMODIFIED indica que no se ha cambiado un mensaje desde la entrega. Un cliente no puede borrar este valor después de que lo haya establecido un proveedor de almacenamiento de mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

