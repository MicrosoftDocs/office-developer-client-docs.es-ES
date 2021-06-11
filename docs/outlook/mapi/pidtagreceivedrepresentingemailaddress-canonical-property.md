---
title: Propiedad canónica PidTagReceivedRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEmailAddress
api_type:
- COM
ms.assetid: f85ce31c-f621-47ed-badf-4f59a45ec0a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6916b1148caaf8283c6d7ae64ac2e05deb3ee0c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359104"
---
# <a name="pidtagreceivedrepresentingemailaddress-canonical-property"></a>Propiedad canónica PidTagReceivedRepresentingEmailAddress

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la dirección de correo electrónico del usuario de mensajería representado por el usuario receptor.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W  <br/> |
|Identificador:  <br/> |0x0078  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Dirección  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que está siendo representado por el usuario receptor. Deben ser establecidas por el proveedor de transporte entrante, que también es responsable de la autorización o comprobación del delegado. Si no se representa ningún usuario de mensajería, estas propiedades deben establecerse en la dirección de correo electrónico incluida en la propiedad **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)).
  
Una aplicación cliente que responda a un mensaje recibido en nombre de otro cliente debe copiar estas propiedades del mensaje recibido en la propiedad **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) para la respuesta.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagEmailAddress](pidtagemailaddress-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

