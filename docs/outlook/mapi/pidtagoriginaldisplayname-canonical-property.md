---
title: Propiedad canónica PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355611"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a>Propiedad canónica PidTagOriginalDisplayName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre para mostrar original de una entrada copiada de una libreta de direcciones a una libreta de direcciones personal u otra libreta de direcciones grabable.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x3A13  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades contienen información sobre el origen original de una entrada copiada.
  
Para un informe no leído, estas propiedades contienen una copia del nombre para mostrar del destinatario del mensaje original para el que se genera el informe. Cuando el destinatario original forma parte de una lista de distribución, el nombre para mostrar de la lista de distribución se conserva para el informe.
  
Una aplicación cliente puede usar estas propiedades para evitar la alteración o "suplantación" de entradas, al dar una copia sin modificar del nombre para mostrar para comparar.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

