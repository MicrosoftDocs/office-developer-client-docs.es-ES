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
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820086"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Propiedad canónica PidTagRenderingPosition

  
  
**Hace referencia a**: Outlook 
  
Contiene un desplazamiento, en caracteres, que se usarán en la representación de un archivo adjunto dentro del texto principal del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RENDERING_POSITION  <br/> |
|Identificador:  <br/> |0x370B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando el desplazamiento suministrado es -1 (0xFFFFFFFF), los datos adjuntos no se representan mediante el uso de esta propiedad. Todos los valores que no sea -1 indican la posición dentro de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) en el que se representan los datos adjuntos.
  
 **Nota** El carácter indicado por esta propiedad en **PR_BODY** se ha reemplazado por los datos adjuntos. Normalmente, este carácter es un espacio, aunque también se puede usar un carácter de marcador de posición especial. 
  
Esta propiedad se expresa en caracteres. En algunos juegos de caracteres no es equivalente a bytes. Las aplicaciones de Unicode pueden calcular la posición basada en caracteres de dos bytes. Las aplicaciones del conjunto de caracteres de doble Byte (DBCS) deben analizar el texto hasta el valor de esta propiedad, porque su representación de carácter varía entre uno y dos bytes por carácter.
  
Esta propiedad no debe usarse con texto de formato de texto enriquecido (RTF). La posición de representación se indica en formato RTF mediante una secuencia de escape llamada el marcador de posición de datos adjuntos del objeto. Esta secuencia se compone de la cadena `\objattph` seguido de un solo carácter, normalmente un espacio, que se reemplazará por la representación de los datos adjuntos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

