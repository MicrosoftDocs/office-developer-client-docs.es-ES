---
title: Propiedad canónica PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355653"
---
# <a name="pidtagmessagesize-canonical-property"></a>Propiedad canónica PidTagMessageSize

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la suma, en bytes, de los tamaños de todas las propiedades de un objeto de mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Identificador:  <br/> |0x0E08  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los objetos de mensaje exponán esta propiedad. El tamaño del mensaje indica el número aproximado de bytes que se transfieren cuando el mensaje se mueve de un almacén de mensajes a otro. Al ser la suma de los tamaños de todas las propiedades del objeto message, suele ser considerablemente mayor que el texto del mensaje solo. 
  
La mayoría de los proveedores de almacén de mensajes calculan esta propiedad para los mensajes que administran. Sin embargo, algunos proveedores de almacén de mensajes no admiten esta propiedad. En cualquier caso, esta propiedad no está disponible hasta que se haya llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

