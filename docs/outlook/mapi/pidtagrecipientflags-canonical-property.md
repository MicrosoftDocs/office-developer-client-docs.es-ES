---
title: Propiedad canónico PidTagRecipientFlags
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820025"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propiedad canónico PidTagRecipientFlags

  
  
**Se aplica a**: Outlook 
  
Especifica un campo de bits que describe el estado del destinatario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificador:  <br/> |0x5FFD  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario del transporte  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad no es necesaria. Los siguientes son los indicadores individuales que se pueden establecer.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|S (recipSendable, 0 x 00000001)  <br/> |El destinatario es un asistente de **Sendable** . Esta marca sólo se utiliza en la propiedad **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |El **RecipientRow** en el que se ha configurado esta marca representa el organizador de la reunión.  <br/> |
|Recuperación de emergencia (recipExceptionalResponse, 0 x 00000010)  <br/> |Indica que el asistente le dio una respuesta para la excepción en el que reside este **RecipientRow** . Esta marca sólo se utiliza en un **RecipientRow** de un objeto de incrustación de mensajes de excepción del objeto del organizador de la reunión.  <br/> |
|ED (recipExceptionalDeleted, 0 x 00000020)  <br/> |Indica que aunque la **RecipientRow** existe, debe tratarse como si no lo hace el destinatario correspondiente. Esta marca sólo se utiliza en un **RecipientRow** de un objeto de incrustación de mensajes de excepción del objeto del organizador de la reunión.  <br/> |
|X (reservada, 0x00000040)  <br/> |No se debe establecer.  <br/> |
|X (reservada, 0x00000080)  <br/> |No se debe establecer.  <br/> |
|G (recipOriginal, 0 x 00000100)  <br/> |Indica que el destinatario es un asistente original. Esta marca sólo se utiliza en la propiedad **dispidApptUnsendableRecips** .  <br/> |
|X (reservada, 0 x 00000200)  <br/> |Reservado.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

