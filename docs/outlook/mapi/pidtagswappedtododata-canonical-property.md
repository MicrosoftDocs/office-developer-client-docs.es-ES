---
title: Propiedad canónica PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359139"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propiedad canónica PidTagSwappedToDoData

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mantiene un segundo conjunto de valores de propiedad que no afectan al estado marcado del objeto Message.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificador:  <br/> |0x0E2D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Actuando como ubicación de almacenamiento de marca secundaria si se admiten marcas de remitente o avisos de remitente, esta estructura proporciona una ubicación en la que almacenar todas las propiedades relacionadas con el protocolo de marcación informativo admitidas en las marcas del remitente y todas las propiedades relacionadas con el protocolo de configuración de avisos que se admiten en avisos de remitente sin exponer la marca del remitente o la información de aviso del remitente a los destinatarios de un mensaje.
  
De forma similar, esta estructura proporciona una ubicación en la que almacenar todas las propiedades relacionadas con el protocolo de marcación informativo que se admiten en las marcas de destinatario y las propiedades relacionadas con el protocolo de configuración de aviso que se admiten en los avisos de destinatario en un mensaje enviado anteriormente.
  
Para obtener más información acerca de esta propiedad, [vea [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.
    
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

