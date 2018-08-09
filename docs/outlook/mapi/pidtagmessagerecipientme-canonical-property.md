---
title: Propiedad canónica PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ae52df1dd9775f706e2b1b2dc8b17b1f47a0bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819762"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propiedad canónica PidTagMessageRecipientMe

  
  
**Hace referencia a**: Outlook 
  
Contiene TRUE si este usuario de mensajería específicamente con nombre de un servidor principal (a), copia (CC) o destinatario de copia oculta (CCO) del mensaje y no forma parte de una lista de distribución. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificador:  <br/> |0x0059  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona una forma cómoda para determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios, sin examinar todas las entradas de la lista. El valor representa la operación de **OR** lógica de las propiedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) y **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) y la información de CCO (que no aparece en caso contrario, en una propiedad). 
  
Esta propiedad ayuda a tratamiento automatizado de los mensajes recibidos en el momento de recepción. En la opción del proveedor de transporte, esta propiedad contiene es FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios. 
  
Entrega de mensajes que dan como resultado de la expansión de la lista de distribución no provoca que se establezca esta propiedad. El destinatario debe denominarse explícitamente. 
  
Por lo general los mensajes no enviados no establecer esta propiedad, **PR_MESSAGE_CC_ME**o **PR_MESSAGE_TO_ME**. Si están presentes en los mensajes que puede obtener acceso el usuario en los almacenes de mensajes pública, en privado de los demás usuarios almacenes de archivos en el disco, o incrustado en otros mensajes recibidos, que generalmente contienen los valores a la que se establece la última vez que un proveedor de transporte entregado el mensaje. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

