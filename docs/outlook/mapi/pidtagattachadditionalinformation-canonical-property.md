---
title: Propiedad canónica PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389634"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>Propiedad canónica PidTagAttachAdditionalInformation

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Proporciona información de tipo de archivo para datos adjuntos de que no son de Windows.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Identificador:  <br/> |0x370F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona metadatos sobre un dato adjunto determinado en función de la codificación de los datos adjuntos. Por ejemplo, cuando la propiedad **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contiene MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contiene una cadena que representa el tipo de archivo, con formato como ":CREA:TYPE" y creador de archivo de Macintosh para el archivo codificado de Macintosh. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
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

