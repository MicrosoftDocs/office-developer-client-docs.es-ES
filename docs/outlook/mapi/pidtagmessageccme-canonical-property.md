---
title: Propiedad canónica PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389774"
---
# <a name="pidtagmessageccme-canonical-property"></a>Propiedad canónica PidTagMessageCcMe

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si este usuario de mensajería específicamente con nombre de un destinatario de copia (CC) de este mensaje y no forma parte de una lista de distribución. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Identificador:  <br/> |0x0058  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona una forma cómoda para determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios con copia oculta, sin examinar todas las entradas de la lista. 
  
Esta propiedad también ayuda a tratamiento automatizado de los mensajes recibidos en el momento de recepción. En la opción del proveedor de transporte, esta propiedad contiene es FALSE o no se establece si el usuario de mensajería no aparece directamente en la tabla de destinatarios. 
  
Entrega del mensaje resultante de expansión de lista de distribución o una designación de copia oculta no causa esta propiedad va a establecer. El destinatario debe denominarse explícitamente. 
  
Por lo general, los mensajes no enviados no establezca esta propiedad, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) o **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Si están presentes en los mensajes que puede obtener acceso el usuario en los almacenes de mensajes pública, en privado de los demás usuarios almacenes de archivos en el disco, o incrustado en otros mensajes recibidos, que generalmente contienen los valores a la que se establece la última vez que un proveedor de transporte entregado el mensaje. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

