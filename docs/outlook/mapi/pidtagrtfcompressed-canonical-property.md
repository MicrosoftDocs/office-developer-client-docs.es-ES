---
title: Propiedad canónica PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394898"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propiedad canónica PidTagRtfCompressed

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la versión de formato de texto enriquecido (RTF) del texto del mensaje, normalmente en formato comprimido. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificador:  <br/> |0 x 1009  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene el mismo texto del mensaje como la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), pero en formato RTF. 
  
Texto del mensaje en formato RTF normalmente se almacena en formato comprimido. Sin embargo, algunos sistemas no comprimen el texto con formato. Para dar cabida a ellos, MAPI proporciona el valor de dwMagicUncompressedRTF para un encabezado de la secuencia identificar RTF sin comprimir y la marca **STORE_UNCOMPRESSED_RTF** en **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para el mensaje almacén para indicar que puede almacenar sin comprimir RTF. 
  
Para obtener el contenido de esta propiedad, llamada **OpenProperty**, a continuación, llame al método [WrapCompressedRTFStream](wrapcompressedrtfstream.md) con la marca **MAPI_READ** . Para escribir en esta propiedad, se abre con los indicadores **MAPI_MODIFY** y **MAPI_CREATE** . Esto garantiza que los nuevos datos reemplazan completamente cualquier datos antiguos y que las escrituras se realizan con el número mínimo de almacén de actualizaciones. 
  
Almacenes de mensaje que admiten el formato RTF omitir los cambios realizados en el espacio en blanco en el texto del mensaje. Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena esta propiedad. Si posteriormente se llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y **PR_BODY** se ha modificado, el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión RTF. Si sólo se ha cambiado el espacio en blanco, las propiedades se dejan sin cambios. Esto significa que mantiene cualquier RTF no trivial formato cuando el mensaje se transmite a través de clientes ajenos a RTF y sistemas de mensajería. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codifica y descodifica una secuencia comprimida en cuerpos de mensaje RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsula formatos de contenido adicionales (por ejemplo, HTML) dentro de la propiedad body RTF de mensajes y datos adjuntos.
    
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

