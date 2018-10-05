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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392574"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propiedad canónica PidTagSendInternetEncoding

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de codificación preferencias. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificador:  <br/> |0x3A71  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Establecer esta propiedad para indicar las opciones de codificación utilizadas. 
  
Esta propiedad contiene los siguientes indicadores:
  
BODY_ENCODING_HTML 
  
> Codificar el texto del mensaje en HTML. Este indicador se omite a menos que se establece la marca ENCODING_MIME. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codificar el texto del mensaje con el texto y el código HTML como alternativas de varias partes de extensiones multipropósito de correo Internet (MIME). Este indicador se omite a menos que se establece la marca ENCODING_MIME. 
    
ENCODING_MIME 
  
> Codificar el mensaje con MIME. Si no se establece este marcador, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos de UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Use los otros marcadores de esta máscara de bits para determinar la codificación. Si no se establece este marcador, MAPI deja que el sistema de mensajería para tomar decisiones de codificación. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codificar datos adjuntos de Macintosh en modo doble de Apple. Este indicador se omite a menos que se establece la marca ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codificar datos adjuntos de Macintosh en modo simple de Apple. Este indicador se omite a menos que se establece la marca ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codificar datos adjuntos de Macintosh en UUENCODE. Si se establece la marca ENCODING_MIME, este indicador se omite y codificación BinHex se usa en su lugar. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

