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
  
Contiene TRUE si el destinatario puede recibir todo el contenido del mensaje, incluidos el formato de texto enriquecido (RTF) y los objetos de vinculación e incrustación de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificador:  <br/> |0x3A40  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que la lista de distribución y los objetos de usuario de mensajería expongan esta propiedad. 
  
Esta propiedad indica si el remitente considera que el destinatario está habilitado para MAPI. 
  
Cuando esta propiedad se establece en TRUE, el transporte y la puerta de enlace pueden transmitir el contenido completo del mensaje, incluidos los objetos RTF y OLE. El proveedor de transporte y la puerta de enlace deben usar el formato de encapsulación neutro para el transporte (TNEF) para encapsular las propiedades que no son nativas para todos los sistemas de mensajería involucrados. 
  
Cuando esta propiedad se establece en FALSE, el proveedor de transporte y la puerta de enlace pueden descartar el contenido del mensaje que sus clientes nativos no pueden usar. Por ejemplo, cuando los clientes no admiten RTF, el proveedor de transporte sólo puede enviar texto sin formato. 
  
Cuando no se establece esta propiedad, el comportamiento predeterminado viene determinado por la implementación del proveedor de transporte, el agente de transferencia de mensajes (MTA) o la puerta de enlace. No es necesario que los proveedores de la libreta de direcciones admitan esta propiedad. Por ejemplo, una libreta de direcciones y un proveedor de transporte muy acoplados pueden elegir enviar TNEF pero nunca usar RTF. 
  
El cliente no debe asumir que el proveedor de transporte y la puerta de enlace usarán la TNEF por su propia iniciativa. Algunos proveedores de transporte y puertas de enlace que admiten TNEF lo transmiten sin tener en cuenta el valor de esta propiedad, pero otros rechazan la construcción o el envío de TNEF si no se establece en TRUE. 
  
> [!NOTE]
> El valor de esta propiedad, así como las decisiones basadas en su valor, se deben a cada destinatario. 
  
De forma predeterminada, MAPI establece el valor en TRUE. Un cliente que llama a [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) o un proveedor que llama a [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) puede establecer el bit **MAPI_SEND_NO_RICH_INFO** en el parámetro _ulFlags_ , lo que hace que MAPI establezca esta propiedad en false. Las aprobaciones creadas por la interfaz de usuario usan el valor especificado por la plantilla que la crea. 
  
En las llamadas al método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) cuando no se puede resolver el nombre, pero se puede interpretar como una dirección de Internet (SMTP), esta propiedad se establece en false. Para que se pueda interpretar como una dirección de Internet, el nombre para mostrar de la entrada no resuelta debe tener el formato X @ Y. Z, como "pete@pinecone.com". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> de las convenciones de correo electrónico estándar de Internet a los objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

