---
title: Propiedad canónica PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342675"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propiedad canónica PidTagSendInternetEncoding

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de preferencias de codificación. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificador:  <br/> |0x3A71  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Establezca esta propiedad para indicar las opciones de codificación usadas. 
  
Esta propiedad contiene las siguientes marcas:
  
BODY_ENCODING_HTML 
  
> Codifica el texto del mensaje en HTML. Esta marca se omite a menos que ENCODING_MIME esté establecida. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codificar el texto del mensaje con texto y HTML como alternativas multipart extensions multipropósito al correo de Internet (MIME). Esta marca se omite a menos que ENCODING_MIME esté establecida. 
    
ENCODING_MIME 
  
> Codifica el mensaje con MIME. Si no se establece esta marca, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos en UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Use las otras marcas de esta máscara de bits para determinar la codificación. Si no se establece esta marca, MAPI la deja en el sistema de mensajería para tomar decisiones de codificación. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codificar datos adjuntos de Macintosh en modo doble de Apple. Esta marca se omite a menos que ENCODING_MIME esté establecida. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codificar datos adjuntos de Macintosh en modo único de Apple. Esta marca se omite a menos que ENCODING_MIME esté establecida. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codificar datos adjuntos de Macintosh en UUENCODE. Si se ENCODING_MIME marca predeterminada, esta marca se omite y se usa la codificación BinHex en su lugar. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

