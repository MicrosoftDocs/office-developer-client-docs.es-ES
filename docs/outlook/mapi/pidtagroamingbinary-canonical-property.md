---
title: Propiedad canónica PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359566"
---
# <a name="pidtagroamingbinary-canonical-property"></a>Propiedad canónica PidTagRoamingBinary

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia de mensajes asociada a una subclase de la **IPM.Configde uration.** 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Identificador:  <br/> |0x7C09  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene la secuencia de datos asociada a un **IPM.Configde clase de** mensaje de uration. El formato de la secuencia depende de la clase de mensaje. Por ejemplo, un mensaje de tipo de **claseIPM.Configuration. La autocompletar** tendría el formato de secuencia [de autocompletar](autocomplete-stream.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

