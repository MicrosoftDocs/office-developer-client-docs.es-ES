---
title: Propiedad canónica PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359097"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>Propiedad canónica PidTagReceivedRepresentingEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada del usuario de mensajería representado por el usuario receptor.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|Identificador:  <br/> |0x0043  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una de las propiedades de dirección del usuario de mensajería representado por el usuario receptor. Debe establecerlo el proveedor de transporte entrante, que también es responsable de la autorización o comprobación del delegado. Si no se representa ningún usuario de mensajería, esta propiedad debe establecerse en el identificador de entrada incluido en la **propiedad PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).
  
Una aplicación cliente que responda a un mensaje recibido en nombre de otro cliente debe copiar esta propiedad del mensaje recibido en la propiedad **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) para la respuesta.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

