---
title: Propiedad canónica PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359223"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a>Propiedad canónica PidTagReceivedByEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada del usuario de mensajería que realmente recibe el mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECEIVED_BY_ENTRYID  <br/> |
|Identificador:  <br/> |0x003F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una de las propiedades de dirección del usuario de mensajería que recibe el mensaje. Debe establecerlo el proveedor de transporte entrante.
  
Esta propiedad corresponde a un sobre de entrega X.400 por mensaje MH_T_ mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y elementos de citas y reuniones.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos a una representación de secuencia eficiente.
    
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

