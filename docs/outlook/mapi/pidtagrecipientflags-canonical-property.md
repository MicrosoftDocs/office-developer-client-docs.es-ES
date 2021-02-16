---
title: Propiedad canónica PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356703"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propiedad canónica PidTagRecipientFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un campo de bits que describe el estado del destinatario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificador:  <br/> |0x5FFD  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario de transporte  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no es necesaria. Las siguientes son las marcas individuales que se pueden establecer.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |El destinatario es un **asistente que se puede** enviar. Esta marca solo se usa en la propiedad **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |El **RecipientRow** en el que se establece esta marca representa al organizador de la reunión.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Indica que el asistente ha dado una respuesta para la excepción en la que **reside este RecipientRow.** Esta marca solo se usa en **recipientRow** de un objeto de mensaje incrustado de excepción del objeto de reunión del organizador.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Indica que, aunque **existe RecipientRow,** debe tratarse como si el destinatario correspondiente no lo hubiera hecho. Esta marca solo se usa en **recipientRow** de un objeto de mensaje incrustado de excepción del objeto de reunión del organizador.  <br/> |
|X (reservado, 0x00000040)  <br/> |No se debe establecer.  <br/> |
|X (reservado, 0x00000080)  <br/> |No se debe establecer.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Indica que el destinatario es un asistente original. Esta marca solo se usa en la **propiedad dispidApptUnsendableRecips.**  <br/> |
|X (reservado, 0x00000200)  <br/> |Reservado.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

