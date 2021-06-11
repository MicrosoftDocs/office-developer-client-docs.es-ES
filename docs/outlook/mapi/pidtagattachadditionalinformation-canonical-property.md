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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339878"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>Propiedad canónica PidTagAttachAdditionalInformation

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información de tipo de archivo para datos adjuntos que no Windows datos adjuntos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Identificador:  <br/> |0x370F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona metadatos sobre un dato adjunto determinado en función de la codificación de los datos adjuntos. Por ejemplo, cuando la propiedad **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contiene MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contiene una cadena que representa el creador de archivos de Macintosh y el tipo de archivo, con el formato ":CREA:TYPE" para el archivo Macintosh codificado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
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

