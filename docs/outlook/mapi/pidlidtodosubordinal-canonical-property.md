---
title: Propiedad canónica PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344922"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>Propiedad canónica PidLidToDoSubOrdinal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actúa como separador de empates cuando la propiedad **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) ordena objetos y el resultado es una empate.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidToDoSubOrdinal  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A1  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se usa, esta propiedad debe ordenarse léxicamente. Los caracteres componentes de la cadena deben constar solo de los números de cero a nueve. Esta propiedad debe establecerse inicialmente en "5555555". La longitud de esta propiedad no debe superar los 254 caracteres (excepto el carácter NULL de terminación).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

