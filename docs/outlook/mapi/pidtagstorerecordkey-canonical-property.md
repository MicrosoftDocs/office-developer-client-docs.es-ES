---
title: Propiedad canónica PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08527f3325742eb7c48f11c2ed7d08f71fa3e972
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592713"
---
# <a name="pidtagstorerecordkey-canonical-property"></a>Propiedad canónica PidTagStoreRecordKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador único de binario comparable (clave de registro) del almacén de mensajes en el que reside un objeto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_RECORD_KEY  <br/> |
|Identificador:  <br/> |0x0FFA  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para un almacén de mensajes, esta propiedad es idéntica a la propiedad de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) del almacén.
  
La relación entre esta propiedad y **PR_RECORD_KEY** es la misma que la relación entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

