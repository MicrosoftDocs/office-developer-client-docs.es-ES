---
title: Propiedad canónica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326638"
---
# <a name="pidtagbody-canonical-property"></a>Propiedad canónica PidTagBody

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el texto del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificador:  <br/> |0x1000  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Normalmente, estas propiedades solo se usan en un mensaje interpersonal (IPM). 
  
Los almacenes de mensajes que admiten el formato de texto enriquecido (RTF) omiten los cambios en el espacio en blanco del texto del mensaje. Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena la propiedad **PR_RTF_COMPRESSED** ([PIDTAGRTFCOMPRESSED](pidtagrtfcompressed-canonical-property.md)), la versión rtf del texto del mensaje. Si se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) posteriormente y se ha modificado **PR_BODY** , el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión rtf. Si solo se ha cambiado el espacio en blanco, las propiedades permanecen sin cambios. Esto conserva todo el formato RTF no trivial cuando el mensaje se desplaza a través de clientes no compatibles con RTF y sistemas de mensajería. 
  
El valor de esta propiedad debe expresarse en la página de códigos del sistema operativo en el que se está ejecutando MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

