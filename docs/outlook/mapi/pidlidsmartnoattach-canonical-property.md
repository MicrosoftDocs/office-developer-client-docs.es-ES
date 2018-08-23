---
title: Propiedad canónica PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e4a0e87b24789e3ee4cb5ed6684d508b62e65b30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575976"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Propiedad canónica PidLidSmartNoAttach

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si los datos adjuntos en un mensaje se consideran como ocultas.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSmartNoAttach  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008514  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuración de tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es TRUE si los datos adjuntos del mensaje se consideran como ocultas.
  
Indica si el objeto de mensaje no tiene los datos adjuntos visible para el usuario final. Esta propiedad puede ser sin establecer; Si es así, se supone un valor predeterminado de FALSE.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

