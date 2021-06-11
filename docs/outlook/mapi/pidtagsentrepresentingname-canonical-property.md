---
title: Propiedad canónica PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314934"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a>Propiedad canónica PidTagSentRepresentingName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre para mostrar del usuario de mensajería representado por el remitente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W  <br/> |
|Identificador:  <br/> |0x0042  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Dirección  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que representa el remitente. Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente. Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.
  
El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si el cliente de envío la ha establecido. Si no se establece, el proveedor de transporte debe establecerlo en **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)
  
> Especifica las propiedades y las operaciones que representan elementos RSS.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos post.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para los objetos de lista de distribución personal y de contacto.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

