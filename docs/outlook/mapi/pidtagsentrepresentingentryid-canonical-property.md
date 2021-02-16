---
title: Propiedad canónica PidTagSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359090"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a>Propiedad canónica PidTagSentRepresentingEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada del usuario de mensajería representado por el remitente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SENT_REPRESENTING_ENTRYID  <br/> |
|Identificador:  <br/> |0x0041  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una de las propiedades de dirección del usuario de mensajería que representa el remitente. Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente. Un usuario de mensajería que envía en su propio nombre normalmente deja sin conjunto las propiedades del remitente representado.
  
El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si la ha establecido el cliente de envío. Si no se establece, el proveedor de transporte debe establecerlo en **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos post.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

