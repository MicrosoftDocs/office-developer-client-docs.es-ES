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
  
Contiene una máscara de código de las preferencias de codificación. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificador:  <br/> |0x3A71  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Establezca esta propiedad para indicar las opciones de codificación utilizadas. 
  
Esta propiedad contiene los siguientes indicadores:
  
BODY_ENCODING_HTML 
  
> Codifique el texto del mensaje en HTML. Esta marca se omite a menos que se establezca la marca ENCODING_MIME. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codifique el texto del mensaje usando Text y HTML como alternativas multipropósito de Multipurpose Internet Mail Extensions (MIME). Esta marca se omite a menos que se establezca la marca ENCODING_MIME. 
    
ENCODING_MIME 
  
> Codifique el mensaje con MIME. Si no se establece esta marca, MAPI codifica el texto del mensaje como texto sin formato y los datos adjuntos en UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Use el resto de las marcas de esta máscara de la máscara para determinar la codificación. Si no se establece esta marca, MAPI deja el sistema de mensajería para tomar decisiones de codificación. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codificar datos adjuntos Macintosh en el modo doble de Apple. Esta marca se omite a menos que se establezca la marca ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codificar datos adjuntos Macintosh en el modo Single de Apple. Esta marca se omite a menos que se establezca la marca ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codificar datos adjuntos Macintosh en UUENCODE. Si se establece la marca ENCODING_MIME, se omite esta marca y se usa la codificación BinHex en su lugar. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

