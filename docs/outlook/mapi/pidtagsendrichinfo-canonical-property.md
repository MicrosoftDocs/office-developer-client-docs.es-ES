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
ms.openlocfilehash: a1db4ba7a70695b17631ca13f1728043be8164bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575970"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propiedad canónica PidTagSendRichInfo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el destinatario puede recibir todo el contenido mensaje, incluido el formato de texto enriquecido (RTF) y objetos de vinculación e incrustación de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificador:  <br/> |0x3A40  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que la lista de distribución y objetos de usuario de mensajería exponen esta propiedad. 
  
Esta propiedad indica si el remitente tiene en cuenta el destinatario habilitado para MAPI. 
  
Cuando esta propiedad se establece en TRUE, el transporte y la puerta de enlace pueden transmitir el contenido completo del mensaje, incluidos los objetos RTF y OLE. El proveedor de transporte y puerta de enlace deben usar el formato de encapsulación neutro de transporte (TNEF) para encapsular todas las propiedades que no son nativas de todos los sistemas de mensajería implicados. 
  
Cuando esta propiedad se establece en FALSE, el proveedor de transporte y puerta de enlace están libres para descartar el contenido de los mensajes que no se pueden usar sus clientes nativos. Por ejemplo, cuando los clientes no admiten RTF, el proveedor de transporte puede enviar sólo texto sin formato. 
  
Cuando no se establece esta propiedad, el comportamiento predeterminado se determina por la implementación del proveedor de transporte, el agente de transferencia de mensajes (MTA) o la puerta de enlace. Los proveedores de la libreta de direcciones no son necesarios para admitir esta propiedad. Por ejemplo, puede elegir un proveedor de libreta de direcciones y transporte de dirección acoplado enviar TNEF, pero nunca utilizan el formato RTF. 
  
El cliente no debe asumir el proveedor de transporte y puerta de enlace, usa TNEF en su propia iniciativa. Algunos proveedores de transporte y las puertas de enlace que admiten TNEF transmiten sin tener en cuenta el valor de esta propiedad, pero otras personas rechazar construir o enviar TNEF si no está establecido en TRUE. 
  
> [!NOTE]
> El valor de esta propiedad así como las decisiones en función de su valor, se encuentran en una base por destinatario. 
  
De forma predeterminada, MAPI establece el valor en TRUE. Un cliente de una llamada a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) o un proveedor de llamar a [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) puede establecer el bit **MAPI_SEND_NO_RICH_INFO** en el parámetro _ulFlags_ , que hace que MAPI establecer esta propiedad en FALSE. Uso único creado por la interfaz de usuario use el valor especificado por la plantilla de creación. 
  
En las llamadas al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) cuando no se puede resolver el nombre, pero se puede interpretar como una dirección de Internet (SMTP), esta propiedad se establece en FALSE. Para interpretarse como una dirección de Internet, debe ser el nombre para mostrar de la entrada sin resolver en el formato X@Y. Z, como "pete@pinecone.com". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> en las convenciones de correo electrónico estándar de Internet para enviar mensajes a objetos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

