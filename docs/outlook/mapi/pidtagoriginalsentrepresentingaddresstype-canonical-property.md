---
title: Propiedad canónica PidTagOriginalSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfb768b774b1fa3d4b65ad2122f49a8ffe11a7b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341226"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a>Propiedad canónica PidTagOriginalSentRepresentingAddressType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de dirección del usuario de mensajería en cuyo nombre se envió el mensaje original.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W  <br/> |
|Identificador:  <br/> |0x0068  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son el tipo para el remitente representado original de un mensaje. Se usan en un hilo de conversación.
  
Una aplicación cliente que envía un mensaje en nombre de otro cliente debe establecer estas propiedades en el valor de la propiedad **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) en el primer envío del mensaje. Una vez establecido, nunca debe cambiarse.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

