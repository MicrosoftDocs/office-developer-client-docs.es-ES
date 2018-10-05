---
title: Propiedad canónica PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388437"
---
# <a name="pidtagattachextension-canonical-property"></a>Propiedad canónica PidTagAttachExtension

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una extensión de nombre de archivo que indica el tipo de documento de un archivo adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Identificador:  <br/> |0x3703  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se establecen mediante la aplicación de cliente en tiempo de envío. 
  
La mensajería usos del sistema **PR_ATTACH_EXTENSION** al convertir los datos adjuntos de mensajes (en la ruta de conversión) o el inicio de aplicaciones en función de los datos adjuntos en los mensajes recibidos. Si el cliente de envío no proporciona un valor para estas propiedades, el almacén de mensajes de tratamiento de los datos adjuntos no está obligado a generarlo. El cliente receptor debe comprobar **PR_ATTACH_EXTENSION**y, si no se proporciona, debe analizar la extensión de nombre de archivo de los datos de adjuntos **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) o **PR_ATTACH_LONG_FILENAME **([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) (propiedad). 
  
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

