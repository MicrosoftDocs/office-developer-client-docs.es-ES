---
title: Propiedad canónica PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355156"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Propiedad canónica PidTagRenderingPosition

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un desplazamiento, en caracteres, que se usa para representar datos adjuntos dentro del texto del mensaje principal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RENDERING_POSITION  <br/> |
|Identificador:  <br/> |0x370B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos mapi  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando el desplazamiento proporcionado es -1 (0xFFFFFFFF), los datos adjuntos no se representan mediante esta propiedad. Todos los valores distintos de -1 indican la posición dentro de **la propiedad PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) en la que se representarán los datos adjuntos.
  
 **Nota** El carácter indicado por esta propiedad en **PR_BODY** se reemplaza por los datos adjuntos. Normalmente, este carácter es un espacio, aunque también se puede usar un carácter de marcador de posición especial. 
  
Esta propiedad se expresa en caracteres. En algunos juegos de caracteres, esto no equivale a bytes. Las aplicaciones Unicode pueden calcular la posición en función de caracteres de dos bytes. Double-Byte de juego de caracteres (DBCS) deben examinar el texto hasta este valor de propiedad, ya que su representación de caracteres varía entre uno y dos bytes por carácter.
  
Esta propiedad no debe usarse con texto en formato de texto enriquecido (RTF). La posición de representación se indica en RTF mediante una secuencia de escape denominada marcador de posición de datos adjuntos del objeto. Esta secuencia consta de la cadena seguida de un solo carácter, normalmente un espacio, que se reemplazará por la  `\objattph` representación de datos adjuntos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
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

