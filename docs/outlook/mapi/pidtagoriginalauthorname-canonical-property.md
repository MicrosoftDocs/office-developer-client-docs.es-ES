---
title: Propiedad canónica PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 05e29f01747e4d5aa2fe0b61e58fa2ba738a53fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592853"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>Propiedad canónica PidTagOriginalAuthorName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre para mostrar del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|Identificador:  <br/> |0x004D  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son ejemplos de las propiedades de dirección para el autor de un mensaje. En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor de **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.
  
Permitir que las propiedades autor original para la conservación de la información desde fuera del dominio de mensajería local. Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

