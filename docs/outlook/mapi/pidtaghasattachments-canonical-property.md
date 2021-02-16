---
title: Propiedad canónica PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316131"
---
# <a name="pidtaghasattachments-canonical-property"></a>Propiedad canónica PidTagHasAttachments

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un mensaje contiene al menos un dato adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_HASATTACH  <br/> |
|Identificador:  <br/> |0x0E1B  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes copia esta propiedad de **la marca MSGFLAG_HASATTACH** de la **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). A continuación, una aplicación cliente **puede PR_HASATTACH** para ordenar los datos adjuntos del mensaje en un visor de mensajes. 
  
El valor de esta propiedad se actualiza con el [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
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

