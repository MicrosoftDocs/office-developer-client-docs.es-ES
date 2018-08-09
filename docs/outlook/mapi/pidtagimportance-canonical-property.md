---
title: Propiedad canónica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819606"
---
# <a name="pidtagimportance-canonical-property"></a>Propiedad canónica PidTagImportance

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor que indica la opinión de la dirección del remitente del mensaje de la importancia de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IMPORTANCE  <br/> |
|Identificador:  <br/> |0x0017  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

No se deben confundir esta propiedad y la propiedad **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)). Importancia indica un valor a los usuarios, mientras que la prioridad indica el orden o la velocidad a la que se debe enviar el mensaje por el software del sistema de mensajería. Normalmente, una mayor prioridad indica un costo mayor. Mayor importancia generalmente se asocia con una presentación diferentes mediante la interfaz de usuario. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
IMPORTANCE_LOW 
  
> El mensaje tiene importancia baja.
    
IMPORTANCE_HIGH 
  
> El mensaje tiene importancia alta.
    
IMPORTANCE_NORMAL 
  
> El mensaje tiene importancia normal.
    
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

