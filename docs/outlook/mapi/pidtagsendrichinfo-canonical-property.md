---
title: Propiedad canónica PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342521"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propiedad canónica PidTagSendRichInfo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el destinatario puede recibir todo el contenido del mensaje, incluidos los objetos rtf (rtf) y de vinculación e incrustación de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificador:  <br/> |0x3A40  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que la lista de distribución y los objetos de usuario de mensajería exponán esta propiedad. 
  
Esta propiedad indica si el remitente considera que el destinatario está habilitado para MAPI. 
  
Cuando esta propiedad se establece en TRUE, el transporte y la puerta de enlace pueden transmitir todo el contenido del mensaje, incluidos los objetos RTF y OLE. El proveedor de transporte y la puerta de enlace deben usar el formato de encapsulamiento neutro de transporte (TNEF) para encapsular las propiedades que no son nativas para todos los sistemas de mensajería implicados. 
  
Cuando esta propiedad se establece en FALSE, el proveedor de transporte y la puerta de enlace pueden descartar contenido de mensajes que sus clientes nativos no pueden usar. Por ejemplo, cuando los clientes no admiten RTF, el proveedor de transporte solo puede enviar texto sin formato. 
  
Cuando no se establece esta propiedad, el comportamiento predeterminado viene determinado por la implementación del proveedor de transporte, el agente de transferencia de mensajes (MTA) o la puerta de enlace. No es necesario que los proveedores de libretas de direcciones admitan esta propiedad. Por ejemplo, un proveedor de transporte y libreta de direcciones estrechamente acoplada puede elegir enviar TNEF pero nunca usar RTF. 
  
El cliente no debe asumir que el proveedor de transporte y la puerta de enlace usarán TNEF por su propia iniciativa. Algunos proveedores de transporte y puertas de enlace compatibles con TNEF lo transmiten sin tener en cuenta el valor de esta propiedad, pero otros rechazan construir o enviar TNEF si no se establece en TRUE. 
  
> [!NOTE]
> La configuración de esta propiedad y las decisiones basadas en su valor se toman por destinatario. 
  
De forma predeterminada, MAPI establece el valor en TRUE. Un cliente que llama a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) o un proveedor que llama a [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) puede establecer el bit MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags,_ lo que hace que MAPI establezca esta propiedad **en** FALSE. Los usos únicos creados por la interfaz de usuario usan el valor especificado por la plantilla de creación. 
  
En las llamadas al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) cuando el nombre no se puede resolver pero se puede interpretar como una dirección de Internet (SMTP), esta propiedad se establece en FALSE. Para que se interprete como una dirección de Internet, el nombre para mostrar de la entrada sin resolver debe tener el formato X@Y. Z, como "pete@pinecone.com". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para los objetos de mensaje de correo electrónico.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

