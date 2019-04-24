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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357893"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propiedad canónica PidTagRtfCompressed

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la versión de formato de texto enriquecido (RTF) del texto del mensaje, normalmente en forma comprimida. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificador:  <br/> |0x1009  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene el mismo texto del mensaje que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pero en RTF. 
  
El texto del mensaje en RTF suele almacenarse en formato comprimido. Sin embargo, algunos sistemas no comprimen el texto con formato. Para acomodarlos, MAPI proporciona el valor dwMagicUncompressedRTF para un encabezado de secuencia para identificar el formato RTF sin comprimir y la marca **STORE_UNCOMPRESSED_RTF** en **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del mensaje. almacenar para indicar que puede almacenar RTF sin comprimir. 
  
Para obtener el contenido de esta propiedad, llame a **OpenProperty**y, a continuación, llame a [WrapCompressedRTFStream](wrapcompressedrtfstream.md) con la marca **MAPI_READ** . Para escribir en esta propiedad, ábrala con los indicadores **MAPI_MODIFY** y **MAPI_CREATE** . Esto garantiza que los nuevos datos reemplacen completamente los datos antiguos y que las escrituras se realizan usando el número mínimo de actualizaciones de almacén. 
  
Los almacenes de mensajes que admiten RTF ignoran los cambios en el espacio en blanco del texto del mensaje. Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena esta propiedad. Si se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) posteriormente y se ha modificado **PR_BODY** , el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión rtf. Si solo se ha cambiado el espacio en blanco, las propiedades permanecen sin cambios. Esto conserva todo el formato RTF no trivial cuando el mensaje se desplaza a través de clientes no compatibles con RTF y sistemas de mensajería. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codifica y descodifica una secuencia comprimida en cuerpos de mensaje RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsula formatos de contenido adicionales (como HTML) en la propiedad RTF Body de los mensajes y datos adjuntos.
    
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

