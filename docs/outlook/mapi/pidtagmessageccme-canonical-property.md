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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329739"
---
# <a name="pidtagmessageccme-canonical-property"></a>Propiedad canónica PidTagMessageCcMe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si este usuario de mensajería tiene el nombre específico de un destinatario de copia (CC) de este mensaje y no forma parte de una lista de distribución. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Identificador:  <br/> |0x0058  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona una forma cómoda de determinar si el nombre de usuario aparece de forma explícita en la lista de destinatarios con copia carbón, sin examinar todas las entradas de la lista. 
  
Esta propiedad también ayuda a controlar de forma automática los mensajes recibidos en el momento de la recepción. En la opción del proveedor de transporte, esta propiedad ya contiene FALSE o no se establece si el usuario de mensajería no aparece directamente en la tabla de destinatarios. 
  
La entrega de mensajes resultante de la expansión de la lista de distribución o una designación de copia oculta no hace que se establezca esta propiedad. El destinatario debe tener un nombre explícito. 
  
Por lo general, los mensajes no enviados no establecen esta propiedad, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) o **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Si están presentes en los mensajes a los que el usuario puede tener acceso en los almacenes públicos de mensajes, en los almacenes privados de otros usuarios o en los archivos del disco, o incrustados dentro de otros mensajes recibidos, suelen contener los valores para los que se establecieron la última vez que un proveedor de transporte entregó el mensaje. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

