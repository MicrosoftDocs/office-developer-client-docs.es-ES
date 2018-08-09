---
title: Propiedad canónica PidTagSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5ff45bb8ae8fa011a8a46e7438dc73bab5649750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820258"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a>Propiedad canónica PidTagSenderAddressType

  
  
**Hace referencia a**: Outlook 
  
Contiene el tipo de dirección de correo electrónico del remitente del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W  <br/> |
|Identificador:  <br/> |0x0C1E  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son ejemplos de las propiedades de direcciones para el remitente del mensaje. Se debe establecer por el proveedor de transporte saliente, que nunca se debe propagar los valores existentes anteriormente.
  
Si no hay proveedor de transporte ha proporcionado las propiedades de dirección del remitente, la cola MAPI intenta rellenar llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada. Si se han proporcionado sin los identificadores de entrada, la cola MAPI almacena a "Unknown" en todas las propiedades de dirección de remitente del tipo PT_TSTRING. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para registrar objetos.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
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

